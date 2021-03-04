---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/resolve-azerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Resolve-AzError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Resolve-AzError.md
ms.openlocfilehash: e57eaed9865eacc6d783e6895bd3995c1b6a37ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885953"
---
# <span data-ttu-id="1aa8e-101">Resolve-AzError</span><span class="sxs-lookup"><span data-stu-id="1aa8e-101">Resolve-AzError</span></span>

## <span data-ttu-id="1aa8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa8e-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa8e-103">Exibir informações detalhadas sobre erros do PowerShell, com detalhes estendidos para erros do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

## <span data-ttu-id="1aa8e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1aa8e-104">SYNTAX</span></span>

### <span data-ttu-id="1aa8e-105">AnyErrorParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1aa8e-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aa8e-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa8e-106">LastErrorParameterSet</span></span>
```
Resolve-AzError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aa8e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1aa8e-107">DESCRIPTION</span></span>
<span data-ttu-id="1aa8e-108">Resolve e exibe informações detalhadas sobre erros na sessão atual do PowerShell, incluindo onde ocorreu o erro no script, rastreamento de pilha e todas as exceções internas e agregadas.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="1aa8e-109">Para erros do Azure PowerShell, fornece detalhes adicionais sobre problemas de serviço de depuração, incluindo detalhes completos sobre a solicitação e a resposta do servidor que causaram o erro.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="1aa8e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1aa8e-110">EXAMPLES</span></span>

### <span data-ttu-id="1aa8e-111">Exemplo 1: Resolver o último erro</span><span class="sxs-lookup"><span data-stu-id="1aa8e-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzError -Last

   HistoryId: 3


Message        : Run Connect-AzAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzSubscription}
Line           : Get-AzSubscription
Position       : At line:1 char:1
                 + Get-AzSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="1aa8e-112">Obter detalhes do último erro.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-112">Get details of the last error.</span></span>

### <span data-ttu-id="1aa8e-113">Exemplo 2: Resolver todos os erros na sessão</span><span class="sxs-lookup"><span data-stu-id="1aa8e-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzStorageAccount}
Line           : Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8


   HistoryId: 5


Message        : Run Connect-AzAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in C:\zd\azur
                 e-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in
                 C:\zd\azure-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:lin
                 e 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in C:\zd\azure-p
                 owershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in C:\zd\azure-
                 powershell\src\ResourceManager\Profile\Commands.Profile\Subscription\GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzSubscription}
Line           : Get-AzSubscription
Position       : At line:1 char:1
                 + Get-AzSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="1aa8e-114">Obter detalhes de todos os erros que ocorreram na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="1aa8e-115">Exemplo 3: Resolver um erro específico</span><span class="sxs-lookup"><span data-stu-id="1aa8e-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzStorageAccount}
Line           : Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8
```

<span data-ttu-id="1aa8e-116">Obter detalhes do erro especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-116">Get details of the specified error.</span></span>

## <span data-ttu-id="1aa8e-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1aa8e-117">PARAMETERS</span></span>

### <span data-ttu-id="1aa8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa8e-118">-DefaultProfile</span></span>
<span data-ttu-id="1aa8e-119">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1aa8e-119">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa8e-120">-Error</span><span class="sxs-lookup"><span data-stu-id="1aa8e-120">-Error</span></span>
<span data-ttu-id="1aa8e-121">Um ou mais registros de erro a resolver.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-121">One or more error records to resolve.</span></span>  <span data-ttu-id="1aa8e-122">Se nenhum parâmetro for especificado, todos os erros na sessão serão resolvidos.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-122">If no parameters are specified, all errors in the session are resolved.</span></span>

```yaml
Type: System.Management.Automation.ErrorRecord[]
Parameter Sets: AnyErrorParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa8e-123">-Last</span><span class="sxs-lookup"><span data-stu-id="1aa8e-123">-Last</span></span>
<span data-ttu-id="1aa8e-124">Resolva apenas o último erro que ocorreu na sessão.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-124">Resolve only the last error that occurred in the session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LastErrorParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa8e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa8e-125">CommonParameters</span></span>
<span data-ttu-id="1aa8e-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa8e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa8e-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1aa8e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa8e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1aa8e-128">INPUTS</span></span>

### <span data-ttu-id="1aa8e-129">System.Management.Automation.ErrorRecord[]</span><span class="sxs-lookup"><span data-stu-id="1aa8e-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="1aa8e-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1aa8e-130">OUTPUTS</span></span>

### <span data-ttu-id="1aa8e-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span><span class="sxs-lookup"><span data-stu-id="1aa8e-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>

### <span data-ttu-id="1aa8e-132">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="1aa8e-132">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>

### <span data-ttu-id="1aa8e-133">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="1aa8e-133">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>

## <span data-ttu-id="1aa8e-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="1aa8e-134">NOTES</span></span>

## <span data-ttu-id="1aa8e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1aa8e-135">RELATED LINKS</span></span>
