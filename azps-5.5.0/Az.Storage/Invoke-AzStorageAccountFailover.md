---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116339"
---
# <span data-ttu-id="5d56c-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="5d56c-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="5d56c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d56c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d56c-103">Invoca o failover de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5d56c-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="5d56c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d56c-104">SYNTAX</span></span>

### <span data-ttu-id="5d56c-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5d56c-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d56c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5d56c-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d56c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d56c-107">DESCRIPTION</span></span>
<span data-ttu-id="5d56c-108">Invoca o failover de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5d56c-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="5d56c-109">A solicitação de failover pode ser acionada para uma conta de armazenamento em caso de problemas de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5d56c-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="5d56c-110">O failover ocorre do cluster principal da conta de armazenamento para o cluster secundário para contas RA-GRS.</span><span class="sxs-lookup"><span data-stu-id="5d56c-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="5d56c-111">O cluster secundário se tornará principal após o failover.</span><span class="sxs-lookup"><span data-stu-id="5d56c-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="5d56c-112">Entenda o seguinte impacto na sua conta de armazenamento antes de iniciar o failover: 1.1.</span><span class="sxs-lookup"><span data-stu-id="5d56c-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="5d56c-113">Verifique a Última Hora de Sincronização usando AS Estatísticas de Serviço GET Blob ( , GET Table Service Stats ( e https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) GET Queue Service https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) Stats ( para sua https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) conta.</span><span class="sxs-lookup"><span data-stu-id="5d56c-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="5d56c-114">Esses são os dados que você pode perder se iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="5d56c-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="5d56c-115">2.Após o failover, o tipo de conta de armazenamento será convertido em LRS (armazenamento localmente redundante).</span><span class="sxs-lookup"><span data-stu-id="5d56c-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="5d56c-116">Você pode converter sua conta para usar o armazenamento geo-redundante (PGS).</span><span class="sxs-lookup"><span data-stu-id="5d56c-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="5d56c-117">3. Depois que você habilitar novamente o GRS para sua conta de armazenamento, a Microsoft replicará os dados para a nova região secundária.</span><span class="sxs-lookup"><span data-stu-id="5d56c-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="5d56c-118">O tempo de replicação depende da quantidade de dados a ser replicado.</span><span class="sxs-lookup"><span data-stu-id="5d56c-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="5d56c-119">Observe que há cobranças de largura de banda para a bootstrap.</span><span class="sxs-lookup"><span data-stu-id="5d56c-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="5d56c-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="5d56c-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="5d56c-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d56c-121">EXAMPLES</span></span>

### <span data-ttu-id="5d56c-122">Exemplo 1: failover invocado de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5d56c-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="5d56c-123">Esse comando verifica o último tempo de sincronização de uma conta de Armazenamento e, em seguida, inscreva o failover dela, o cluster secundário se tornará principal após o failover.</span><span class="sxs-lookup"><span data-stu-id="5d56c-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="5d56c-124">Como o failover leva muito tempo, sugerimos que ele seja executado no back-end com o parâmetro -As job e aguarde a conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d56c-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="5d56c-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d56c-125">PARAMETERS</span></span>

### <span data-ttu-id="5d56c-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d56c-126">-AsJob</span></span>
<span data-ttu-id="5d56c-127">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5d56c-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d56c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d56c-128">-DefaultProfile</span></span>
<span data-ttu-id="5d56c-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d56c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d56c-130">-Forçar</span><span class="sxs-lookup"><span data-stu-id="5d56c-130">-Force</span></span>
<span data-ttu-id="5d56c-131">Forçar o Failover da Conta</span><span class="sxs-lookup"><span data-stu-id="5d56c-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="5d56c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d56c-132">-InputObject</span></span>
<span data-ttu-id="5d56c-133">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5d56c-133">Storage account object</span></span>

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

### <span data-ttu-id="5d56c-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d56c-134">-Name</span></span>
<span data-ttu-id="5d56c-135">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5d56c-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="5d56c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d56c-136">-ResourceGroupName</span></span>
<span data-ttu-id="5d56c-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d56c-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="5d56c-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5d56c-138">-Confirm</span></span>
<span data-ttu-id="5d56c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d56c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d56c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d56c-140">-WhatIf</span></span>
<span data-ttu-id="5d56c-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5d56c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d56c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d56c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d56c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d56c-143">CommonParameters</span></span>
<span data-ttu-id="5d56c-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d56c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d56c-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d56c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d56c-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="5d56c-146">INPUTS</span></span>

### <span data-ttu-id="5d56c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5d56c-147">System.String</span></span>

## <span data-ttu-id="5d56c-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="5d56c-148">OUTPUTS</span></span>

### <span data-ttu-id="5d56c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d56c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5d56c-150">Notas</span><span class="sxs-lookup"><span data-stu-id="5d56c-150">NOTES</span></span>

## <span data-ttu-id="5d56c-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d56c-151">RELATED LINKS</span></span>
