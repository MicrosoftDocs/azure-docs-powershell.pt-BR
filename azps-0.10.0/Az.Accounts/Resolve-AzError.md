---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/resolve-azerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Resolve-AzError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Resolve-AzError.md
ms.openlocfilehash: e0e4edcf29a0517dc0b8d69e38233817a7874ad9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775238"
---
# <span data-ttu-id="22c16-101">Resolve-AzError</span><span class="sxs-lookup"><span data-stu-id="22c16-101">Resolve-AzError</span></span>

## <span data-ttu-id="22c16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22c16-102">SYNOPSIS</span></span>
<span data-ttu-id="22c16-103">Exibir informações detalhadas sobre erros do PowerShell, com detalhes estendidos para erros do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="22c16-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

## <span data-ttu-id="22c16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22c16-104">SYNTAX</span></span>

### <span data-ttu-id="22c16-105">AnyErrorParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="22c16-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22c16-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="22c16-106">LastErrorParameterSet</span></span>
```
Resolve-AzError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22c16-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22c16-107">DESCRIPTION</span></span>
<span data-ttu-id="22c16-108">Resolve e exibe informações detalhadas sobre erros na sessão atual do PowerShell, incluindo onde o erro ocorreu em script, rastreamento de pilha e todas as exceções internas e agregadas.</span><span class="sxs-lookup"><span data-stu-id="22c16-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="22c16-109">Para erros do PowerShell do Azure fornece mais detalhes em problemas de serviço de depuração, incluindo detalhes completos sobre a solicitação e a resposta do servidor que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="22c16-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="22c16-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22c16-110">EXAMPLES</span></span>

### <span data-ttu-id="22c16-111">Exemplo 1: resolver o último erro</span><span class="sxs-lookup"><span data-stu-id="22c16-111">Example 1: Resolve the Last Error</span></span>
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

<span data-ttu-id="22c16-112">Obter detalhes do último erro.</span><span class="sxs-lookup"><span data-stu-id="22c16-112">Get details of the last error.</span></span>

### <span data-ttu-id="22c16-113">Exemplo 2: resolver todos os erros na sessão</span><span class="sxs-lookup"><span data-stu-id="22c16-113">Example 2: Resolve all Errors in the Session</span></span>
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

<span data-ttu-id="22c16-114">Obter detalhes de todos os erros ocorridos na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="22c16-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="22c16-115">Exemplo 3: resolver um erro específico</span><span class="sxs-lookup"><span data-stu-id="22c16-115">Example 3: Resolve a Specific Error</span></span>
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

<span data-ttu-id="22c16-116">Obter detalhes do erro especificado.</span><span class="sxs-lookup"><span data-stu-id="22c16-116">Get details of the specified error.</span></span>

## <span data-ttu-id="22c16-117">OS</span><span class="sxs-lookup"><span data-stu-id="22c16-117">PARAMETERS</span></span>

### <span data-ttu-id="22c16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c16-118">-DefaultProfile</span></span>
<span data-ttu-id="22c16-119">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="22c16-119">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22c16-120">-Erro</span><span class="sxs-lookup"><span data-stu-id="22c16-120">-Error</span></span>
<span data-ttu-id="22c16-121">Um ou mais registros de erro a serem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="22c16-121">One or more error records to resolve.</span></span>  <span data-ttu-id="22c16-122">Se nenhum parâmetro for especificado, todos os erros na sessão serão resolvidos.</span><span class="sxs-lookup"><span data-stu-id="22c16-122">If no parameters are specified, all errors in the session are resolved.</span></span>

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

### <span data-ttu-id="22c16-123">-Último</span><span class="sxs-lookup"><span data-stu-id="22c16-123">-Last</span></span>
<span data-ttu-id="22c16-124">Resolva somente o último erro ocorrido na sessão.</span><span class="sxs-lookup"><span data-stu-id="22c16-124">Resolve only the last error that occurred in the session.</span></span>

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

### <span data-ttu-id="22c16-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c16-125">CommonParameters</span></span>
<span data-ttu-id="22c16-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c16-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c16-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22c16-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c16-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22c16-128">INPUTS</span></span>

### <span data-ttu-id="22c16-129">System. Management. Automation. ErrorRecord []</span><span class="sxs-lookup"><span data-stu-id="22c16-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="22c16-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22c16-130">OUTPUTS</span></span>

### <span data-ttu-id="22c16-131">Microsoft. Azure. Commands. Profile. Errors. AzureErrorRecord</span><span class="sxs-lookup"><span data-stu-id="22c16-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>

### <span data-ttu-id="22c16-132">Microsoft. Azure. Commands. Profile. Errors. AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="22c16-132">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>

### <span data-ttu-id="22c16-133">Microsoft. Azure. Commands. Profile. Errors. AzureRestExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="22c16-133">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>

## <span data-ttu-id="22c16-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22c16-134">NOTES</span></span>

## <span data-ttu-id="22c16-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22c16-135">RELATED LINKS</span></span>
