---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112488"
---
# <span data-ttu-id="ec6ef-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec6ef-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="ec6ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec6ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6ef-103">Esse comando cria um ponto de extremidade de nuvem de Sincronização de Arquivos do Azure em um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="ec6ef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec6ef-104">SYNTAX</span></span>

### <span data-ttu-id="ec6ef-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ec6ef-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec6ef-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec6ef-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec6ef-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec6ef-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec6ef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec6ef-108">DESCRIPTION</span></span>
<span data-ttu-id="ec6ef-109">Esse comando cria um ponto de extremidade de nuvem de Sincronização de Arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="ec6ef-110">Um ponto de extremidade de nuvem é uma referência a um compartilhamento de arquivos existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="ec6ef-111">Ele representa o compartilhamento de arquivos e define sua participação na sincronização de todos os arquivos da parte do grupo de sincronização no qual o ponto de extremidade da nuvem foi criado.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="ec6ef-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ec6ef-112">EXAMPLES</span></span>

### <span data-ttu-id="ec6ef-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec6ef-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="ec6ef-114">Um ponto de extremidade de nuvem é membro integral de um grupo de sincronização, este é um exemplo de criação de um grupo de sincronização existente chamado "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="ec6ef-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="ec6ef-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec6ef-115">PARAMETERS</span></span>

### <span data-ttu-id="ec6ef-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec6ef-116">-AsJob</span></span>
<span data-ttu-id="ec6ef-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ec6ef-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec6ef-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="ec6ef-118">-AzureFileShareName</span></span>
<span data-ttu-id="ec6ef-119">Nome de compartilhamento de conta de armazenamento (nome de compartilhamento de arquivos do Azure)</span><span class="sxs-lookup"><span data-stu-id="ec6ef-119">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="ec6ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6ef-120">-DefaultProfile</span></span>
<span data-ttu-id="ec6ef-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec6ef-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec6ef-122">-Name</span></span>
<span data-ttu-id="ec6ef-123">Nome do ponto de extremidade da nuvem.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="ec6ef-124">Quando criado por meio do portal do Azure, o Nome é definido como o nome do arquivo do Azure que ele faz referência.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="ec6ef-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ec6ef-125">-ParentObject</span></span>
<span data-ttu-id="ec6ef-126">Objeto SyncGroup, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ec6ef-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ec6ef-127">-ParentResourceId</span></span>
<span data-ttu-id="ec6ef-128">ID do Recurso Pai do SyncGroup</span><span class="sxs-lookup"><span data-stu-id="ec6ef-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="ec6ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec6ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="ec6ef-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ec6ef-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ec6ef-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="ec6ef-132">ID do Recurso de Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="ec6ef-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="ec6ef-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="ec6ef-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="ec6ef-134">ID do Locatário de Conta de Armazenamento (ID do Diretório da Empresa)</span><span class="sxs-lookup"><span data-stu-id="ec6ef-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="ec6ef-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ec6ef-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="ec6ef-136">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ec6ef-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ec6ef-137">-SyncGroupName</span></span>
<span data-ttu-id="ec6ef-138">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ec6ef-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ec6ef-139">-Confirm</span></span>
<span data-ttu-id="ec6ef-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec6ef-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec6ef-141">-WhatIf</span></span>
<span data-ttu-id="ec6ef-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec6ef-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec6ef-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6ef-144">CommonParameters</span></span>
<span data-ttu-id="ec6ef-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec6ef-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6ef-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec6ef-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6ef-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="ec6ef-147">INPUTS</span></span>

### <span data-ttu-id="ec6ef-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ec6ef-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="ec6ef-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ec6ef-149">System.String</span></span>

## <span data-ttu-id="ec6ef-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="ec6ef-150">OUTPUTS</span></span>

### <span data-ttu-id="ec6ef-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec6ef-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="ec6ef-152">Notas</span><span class="sxs-lookup"><span data-stu-id="ec6ef-152">NOTES</span></span>

## <span data-ttu-id="ec6ef-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec6ef-153">RELATED LINKS</span></span>
