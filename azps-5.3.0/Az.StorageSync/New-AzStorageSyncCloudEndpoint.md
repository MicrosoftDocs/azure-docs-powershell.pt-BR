---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271274"
---
# <span data-ttu-id="af71a-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="af71a-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="af71a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af71a-102">SYNOPSIS</span></span>
<span data-ttu-id="af71a-103">Esse comando cria um ponto de extremidade da nuvem do Azure File Sync em um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="af71a-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="af71a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af71a-104">SYNTAX</span></span>

### <span data-ttu-id="af71a-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="af71a-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af71a-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="af71a-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af71a-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="af71a-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af71a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af71a-108">DESCRIPTION</span></span>
<span data-ttu-id="af71a-109">Esse comando cria um ponto de extremidade de nuvem do Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="af71a-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="af71a-110">Um ponto de extremidade de nuvem é uma referência a um compartilhamento de arquivos existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="af71a-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="af71a-111">Ele representa o compartilhamento de arquivos e define a participação na sincronização de todos os arquivos que fazem parte do grupo de sincronização no qual o ponto de extremidade da nuvem foi criado.</span><span class="sxs-lookup"><span data-stu-id="af71a-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="af71a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af71a-112">EXAMPLES</span></span>

### <span data-ttu-id="af71a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af71a-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="af71a-114">Um ponto de extremidade de nuvem é um membro integrante de um grupo de sincronização, este é um exemplo de como criar um grupo de sincronização existente chamado "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="af71a-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="af71a-115">OS</span><span class="sxs-lookup"><span data-stu-id="af71a-115">PARAMETERS</span></span>

### <span data-ttu-id="af71a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af71a-116">-AsJob</span></span>
<span data-ttu-id="af71a-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="af71a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af71a-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="af71a-118">-AzureFileShareName</span></span>
<span data-ttu-id="af71a-119">Nome de compartilhamento de conta de armazenamento (nome de compartilhamento de arquivos do Azure)</span><span class="sxs-lookup"><span data-stu-id="af71a-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af71a-120">-DefaultProfile</span></span>
<span data-ttu-id="af71a-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af71a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af71a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="af71a-122">-Name</span></span>
<span data-ttu-id="af71a-123">Nome do ponto de extremidade da nuvem.</span><span class="sxs-lookup"><span data-stu-id="af71a-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="af71a-124">Quando criado por meio do portal do Azure, o nome é definido como o nome do compartilhamento de arquivos do Azure ao qual ele faz referência.</span><span class="sxs-lookup"><span data-stu-id="af71a-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="af71a-125">-ParentObject</span></span>
<span data-ttu-id="af71a-126">Objeto de objeto de sincronização, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="af71a-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="af71a-127">-ParentResourceId</span></span>
<span data-ttu-id="af71a-128">ID do recurso pai do pool de sincronização</span><span class="sxs-lookup"><span data-stu-id="af71a-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af71a-129">-ResourceGroupName</span></span>
<span data-ttu-id="af71a-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af71a-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="af71a-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="af71a-132">ID do recurso da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="af71a-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="af71a-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="af71a-134">ID de locatário da conta de armazenamento (ID do diretório da empresa)</span><span class="sxs-lookup"><span data-stu-id="af71a-134">Storage Account Tenant Id (Company Directory Id)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="af71a-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="af71a-136">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="af71a-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="af71a-137">-SyncGroupName</span></span>
<span data-ttu-id="af71a-138">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="af71a-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af71a-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af71a-139">-Confirm</span></span>
<span data-ttu-id="af71a-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af71a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af71a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af71a-141">-WhatIf</span></span>
<span data-ttu-id="af71a-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af71a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af71a-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af71a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af71a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af71a-144">CommonParameters</span></span>
<span data-ttu-id="af71a-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af71a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af71a-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af71a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af71a-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af71a-147">INPUTS</span></span>

### <span data-ttu-id="af71a-148">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="af71a-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="af71a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="af71a-149">System.String</span></span>

## <span data-ttu-id="af71a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af71a-150">OUTPUTS</span></span>

### <span data-ttu-id="af71a-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="af71a-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="af71a-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af71a-152">NOTES</span></span>

## <span data-ttu-id="af71a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af71a-153">RELATED LINKS</span></span>
