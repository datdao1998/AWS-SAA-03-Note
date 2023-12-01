**Amazon SWF** provides useful guarantees around task assignments. It ensures that a task is never duplicated and is assigned only once. 

Thus, even though you may have multiple workers for a particular activity type (or a number of instances of a decider), Amazon SWF will give a specific task to only one worker (or one decider instance). 

Additionally, Amazon SWF keeps at most one decision task outstanding at a time for workflow execution. Thus, you can run multiple decider instances without worrying about two instances operating on the same execution simultaneously. These facilities enable you to coordinate your workflow without worrying about duplicate, lost, or conflicting tasks.