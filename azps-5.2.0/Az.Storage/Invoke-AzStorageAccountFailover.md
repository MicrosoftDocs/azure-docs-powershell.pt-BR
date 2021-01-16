---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256975"
---
# <span data-ttu-id="fab8d-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="fab8d-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="fab8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fab8d-102">SYNOPSIS</span></span>
<span data-ttu-id="fab8d-103">Invoca o failover de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fab8d-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="fab8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fab8d-104">SYNTAX</span></span>

### <span data-ttu-id="fab8d-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fab8d-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fab8d-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="fab8d-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fab8d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fab8d-107">DESCRIPTION</span></span>
<span data-ttu-id="fab8d-108">Invoca o failover de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fab8d-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="fab8d-109">A solicitação de failover pode ser disparada para uma conta de armazenamento em caso de problemas de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="fab8d-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="fab8d-110">O failover ocorre do cluster primário da conta de armazenamento para o cluster secundário para contas RA-GRS.</span><span class="sxs-lookup"><span data-stu-id="fab8d-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="fab8d-111">O cluster secundário se tornará primário após o failover.</span><span class="sxs-lookup"><span data-stu-id="fab8d-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="fab8d-112">Compreenda o seguinte impacto para a sua conta de armazenamento antes de iniciar o failover: 1,1.</span><span class="sxs-lookup"><span data-stu-id="fab8d-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="fab8d-113">Verifique o horário da última sincronização usando obter estatísticas de serviço de BLOB ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) , obter estatísticas de serviço de tabela ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) e obter estatísticas de serviço da fila ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) para a sua conta.</span><span class="sxs-lookup"><span data-stu-id="fab8d-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="fab8d-114">Estes são os dados que você pode perder se iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="fab8d-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="fab8d-115">2. após o failover, o tipo de conta de armazenamento será convertido em armazenamento redundante localmente (LRS).</span><span class="sxs-lookup"><span data-stu-id="fab8d-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="fab8d-116">Você pode converter sua conta para usar o armazenamento de redundância geográfica (GRS).</span><span class="sxs-lookup"><span data-stu-id="fab8d-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="fab8d-117">3. depois que você reativar o GRS para sua conta de armazenamento, a Microsoft replicará os dados para a sua nova região secundária.</span><span class="sxs-lookup"><span data-stu-id="fab8d-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="fab8d-118">O tempo de replicação depende do volume de dados a ser replicado.</span><span class="sxs-lookup"><span data-stu-id="fab8d-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="fab8d-119">Observe que há cobranças de largura de banda para a bootstrap.</span><span class="sxs-lookup"><span data-stu-id="fab8d-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="fab8d-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="fab8d-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="fab8d-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fab8d-121">EXAMPLES</span></span>

### <span data-ttu-id="fab8d-122">Exemplo 1: invocar failover de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fab8d-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="fab8d-123">Esse comando verifica o último tempo de sincronização de uma conta de armazenamento e, em seguida, invoca o failover dela, o cluster secundário se tornará primário após o failover.</span><span class="sxs-lookup"><span data-stu-id="fab8d-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="fab8d-124">Como o failover demora muito tempo, sugira para executá-lo no back-end com o parâmetro AsJob e aguarde a conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="fab8d-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="fab8d-125">OS</span><span class="sxs-lookup"><span data-stu-id="fab8d-125">PARAMETERS</span></span>

### <span data-ttu-id="fab8d-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fab8d-126">-AsJob</span></span>
<span data-ttu-id="fab8d-127">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fab8d-127">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab8d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab8d-128">-DefaultProfile</span></span>
<span data-ttu-id="fab8d-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fab8d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab8d-130">-Force</span><span class="sxs-lookup"><span data-stu-id="fab8d-130">-Force</span></span>
<span data-ttu-id="fab8d-131">Forçar o failover da conta</span><span class="sxs-lookup"><span data-stu-id="fab8d-131">Force to Failover the Account</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab8d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fab8d-132">-InputObject</span></span>
<span data-ttu-id="fab8d-133">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fab8d-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fab8d-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="fab8d-134">-Name</span></span>
<span data-ttu-id="fab8d-135">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fab8d-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab8d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab8d-136">-ResourceGroupName</span></span>
<span data-ttu-id="fab8d-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fab8d-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab8d-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fab8d-138">-Confirm</span></span>
<span data-ttu-id="fab8d-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fab8d-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab8d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab8d-140">-WhatIf</span></span>
<span data-ttu-id="fab8d-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fab8d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab8d-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fab8d-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab8d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab8d-143">CommonParameters</span></span>
<span data-ttu-id="fab8d-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab8d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab8d-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab8d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab8d-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fab8d-146">INPUTS</span></span>

### <span data-ttu-id="fab8d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fab8d-147">System.String</span></span>

## <span data-ttu-id="fab8d-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fab8d-148">OUTPUTS</span></span>

### <span data-ttu-id="fab8d-149">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fab8d-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fab8d-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fab8d-150">NOTES</span></span>

## <span data-ttu-id="fab8d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fab8d-151">RELATED LINKS</span></span>
