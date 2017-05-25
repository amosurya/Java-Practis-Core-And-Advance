package com.thread;

import java.util.ArrayList;
import java.util.Date;
import java.util.List;
import java.util.concurrent.Callable;
import java.util.concurrent.ExecutionException;
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
import java.util.concurrent.Future;

class CallableThread implements Callable<String> {

	@Override
	public String call() throws Exception {
		for (int i = 0; i < 5; i++) {
			System.out.println(i);
		}
		Thread.sleep(1000);
		return Thread.currentThread().getName();
	}


}

public class CallableThreadmain {

	public static void main(String[] args) {
			ExecutorService executor = Executors.newFixedThreadPool(6);
			List<Future<String>> list = new ArrayList<>();	
			Callable<String> callable = new CallableThread();
			
			for(int i=0; i< 15; i++){
	            Future<String> future = executor.submit(callable);
	            list.add(future);
	            System.out.println(new Date()+ "::"+(Future<String>)future);
	        }
			
		
			
			executor.shutdown();

	}

}
