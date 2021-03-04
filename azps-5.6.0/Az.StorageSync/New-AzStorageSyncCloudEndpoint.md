---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: c55b49052ae34eba9dfff960c85e9ade7617d2a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893079"
---
# <span data-ttu-id="0112e-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="0112e-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="0112e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0112e-102">SYNOPSIS</span></span>
<span data-ttu-id="0112e-103">Este comando cria um ponto de extremidade de nuvem de sincronização de arquivos do Azure em um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="0112e-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="0112e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0112e-104">SYNTAX</span></span>

### <span data-ttu-id="0112e-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0112e-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0112e-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0112e-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0112e-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0112e-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0112e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0112e-108">DESCRIPTION</span></span>
<span data-ttu-id="0112e-109">Este comando cria um ponto de extremidade de nuvem de Sincronização de Arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0112e-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="0112e-110">Um ponto de extremidade de nuvem é uma referência a um compartilhamento de arquivos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="0112e-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="0112e-111">Ele representa o compartilhamento de arquivos e define sua participação na sincronização de todos os arquivos do grupo de sincronização no qual o ponto de extremidade da nuvem foi criado.</span><span class="sxs-lookup"><span data-stu-id="0112e-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="0112e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0112e-112">EXAMPLES</span></span>

### <span data-ttu-id="0112e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0112e-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="0112e-114">Um ponto de extremidade de nuvem é um membro integral de um grupo de sincronização, este é um exemplo de criação de um dentro de um grupo de sincronização existente chamado "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="0112e-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="0112e-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0112e-115">PARAMETERS</span></span>

### <span data-ttu-id="0112e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0112e-116">-AsJob</span></span>
<span data-ttu-id="0112e-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0112e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0112e-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="0112e-118">-AzureFileShareName</span></span>
<span data-ttu-id="0112e-119">Nome do Compartilhamento de Conta de Armazenamento (nome do compartilhamento de arquivos do Azure)</span><span class="sxs-lookup"><span data-stu-id="0112e-119">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="0112e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0112e-120">-DefaultProfile</span></span>
<span data-ttu-id="0112e-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0112e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0112e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0112e-122">-Name</span></span>
<span data-ttu-id="0112e-123">Nome do ponto de extremidade da nuvem.</span><span class="sxs-lookup"><span data-stu-id="0112e-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="0112e-124">Quando criado por meio do portal do Azure, Name é definido como o nome do arquivo do Azure que ele faz referência.</span><span class="sxs-lookup"><span data-stu-id="0112e-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="0112e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0112e-125">-ParentObject</span></span>
<span data-ttu-id="0112e-126">Objeto SyncGroup, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0112e-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0112e-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0112e-127">-ParentResourceId</span></span>
<span data-ttu-id="0112e-128">ID do Recurso Pai do SyncGroup</span><span class="sxs-lookup"><span data-stu-id="0112e-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="0112e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0112e-129">-ResourceGroupName</span></span>
<span data-ttu-id="0112e-130">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="0112e-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="0112e-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0112e-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="0112e-132">ID do Recurso de Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="0112e-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="0112e-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="0112e-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="0112e-134">ID do Locatário de Conta de Armazenamento (ID do Diretório da Empresa)</span><span class="sxs-lookup"><span data-stu-id="0112e-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="0112e-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0112e-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="0112e-136">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="0112e-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0112e-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0112e-137">-SyncGroupName</span></span>
<span data-ttu-id="0112e-138">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="0112e-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="0112e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0112e-139">-Confirm</span></span>
<span data-ttu-id="0112e-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0112e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0112e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0112e-141">-WhatIf</span></span>
<span data-ttu-id="0112e-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0112e-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0112e-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0112e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0112e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0112e-144">CommonParameters</span></span>
<span data-ttu-id="0112e-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0112e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0112e-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0112e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0112e-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0112e-147">INPUTS</span></span>

### <span data-ttu-id="0112e-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0112e-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="0112e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="0112e-149">System.String</span></span>

## <span data-ttu-id="0112e-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0112e-150">OUTPUTS</span></span>

### <span data-ttu-id="0112e-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="0112e-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="0112e-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="0112e-152">NOTES</span></span>

## <span data-ttu-id="0112e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0112e-153">RELATED LINKS</span></span>
