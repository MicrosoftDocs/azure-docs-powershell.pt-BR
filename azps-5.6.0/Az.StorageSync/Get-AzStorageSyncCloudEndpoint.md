---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: b4dbee18ef0fad33180e9cc9c3d04a49e1288b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888032"
---
# <span data-ttu-id="dcce6-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcce6-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="dcce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcce6-102">SYNOPSIS</span></span>
<span data-ttu-id="dcce6-103">Este comando lista todos os pontos de extremidade da nuvem em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="dcce6-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="dcce6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dcce6-104">SYNTAX</span></span>

### <span data-ttu-id="dcce6-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dcce6-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcce6-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcce6-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcce6-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcce6-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcce6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dcce6-108">DESCRIPTION</span></span>
<span data-ttu-id="dcce6-109">Este comando lista todos os pontos de extremidade da nuvem em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="dcce6-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="dcce6-110">Ele também pode ser usado para listar os atributos de cada ponto de extremidade da nuvem.</span><span class="sxs-lookup"><span data-stu-id="dcce6-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="dcce6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcce6-111">EXAMPLES</span></span>

### <span data-ttu-id="dcce6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcce6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="dcce6-113">Esse comando obtém todos os pontos de extremidade de nuvem contidos no grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="dcce6-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="dcce6-114">Especifique -CloudEndpointName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="dcce6-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="dcce6-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dcce6-115">PARAMETERS</span></span>

### <span data-ttu-id="dcce6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcce6-116">-DefaultProfile</span></span>
<span data-ttu-id="dcce6-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcce6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcce6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="dcce6-118">-Name</span></span>
<span data-ttu-id="dcce6-119">Nome do CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dcce6-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcce6-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dcce6-120">-ParentObject</span></span>
<span data-ttu-id="dcce6-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dcce6-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dcce6-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dcce6-122">-ParentResourceId</span></span>
<span data-ttu-id="dcce6-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dcce6-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dcce6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcce6-124">-ResourceGroupName</span></span>
<span data-ttu-id="dcce6-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="dcce6-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcce6-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="dcce6-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="dcce6-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="dcce6-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcce6-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="dcce6-128">-SyncGroupName</span></span>
<span data-ttu-id="dcce6-129">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="dcce6-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcce6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcce6-130">CommonParameters</span></span>
<span data-ttu-id="dcce6-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcce6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcce6-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcce6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcce6-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcce6-133">INPUTS</span></span>

### <span data-ttu-id="dcce6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dcce6-134">System.String</span></span>

### <span data-ttu-id="dcce6-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="dcce6-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="dcce6-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dcce6-136">OUTPUTS</span></span>

### <span data-ttu-id="dcce6-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcce6-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="dcce6-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="dcce6-138">NOTES</span></span>

## <span data-ttu-id="dcce6-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcce6-139">RELATED LINKS</span></span>
