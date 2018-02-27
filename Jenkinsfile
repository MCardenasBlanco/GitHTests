     properties([
      pipelineTriggers([
      [$class: 'GenericTrigger',
        genericVariables: [
         [expressionType: 'JSONPath', key: 'reference', value: '$.ref'],
         [expressionType: 'JSONPath', key: 'base_ref', value: '$.base_ref'],
         [expressionType: 'JSONPath', key: 'action', value: '$.action'],
         [expressionType: 'JSONPath', key: 'created', value: '$.created'],
         [expressionType: 'JSONPath', key: 'commits', value: '$.commits'],
         [expressionType: 'JSONPath', key: 'targetBranch', value: '$.release.target_commitish'],
         [expressionType: 'JSONPath', key: 'tagName', value: '$.release.name'],
         [expressionType: 'JSONPath', key: 'lastCommitMessage', value: '$.commits[0].message'],
         [expressionType: 'JSONPath', key: 'repoName', value: '$.repository.name'],
         [expressionType: 'JSONPath', key: 'repoURL', value: '$.repository.html_url'],
         [expressionType: 'JSONPath', key: 'ownerEmail', value: '$.repository.owner.email'],
         [expressionType: 'JSONPath', key: 'pusherEmail', value: '$.pusher.email'],
         [expressionType: 'JSONPath', key: 'repoSSHURL', value: '$.repository.ssh_url']
        ],
        genericRequestVariables: [
         [key: 'token', regexpFilter: ''],
        ],
        genericHeaderVariables: [
         [key: 'X-GitHub-Event', regexpFilter: '']
        ],
        regexpFilterText: '',
        regexpFilterExpression: ''
      ]
      ])
     ])

	def event = X_GitHub_Event_0
	print event
	print repoName
	def serviceName = repoName

node(){
    print event
	print repoName
}
