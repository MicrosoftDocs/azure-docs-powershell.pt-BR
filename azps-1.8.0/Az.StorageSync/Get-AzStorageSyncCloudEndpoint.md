---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: decf935cd61c052e2e77dd8fd2eadacd7a548974
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598505"
---
# <span data-ttu-id="9cd35-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cd35-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="9cd35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cd35-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd35-103">Esse comando lista todos os pontos de extremidade da nuvem em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="9cd35-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="9cd35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cd35-104">SYNTAX</span></span>

### <span data-ttu-id="9cd35-105">Objectparameterset (padrão)</span><span class="sxs-lookup"><span data-stu-id="9cd35-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd35-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cd35-106">StringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd35-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cd35-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cd35-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9cd35-108">DESCRIPTION</span></span>
<span data-ttu-id="9cd35-109">Esse comando lista todos os pontos de extremidade da nuvem em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="9cd35-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="9cd35-110">Ele também pode ser usado para listar os atributos de cada ponto de extremidade da nuvem.</span><span class="sxs-lookup"><span data-stu-id="9cd35-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="9cd35-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cd35-111">EXAMPLES</span></span>

### <span data-ttu-id="9cd35-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9cd35-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="9cd35-113">Esse comando obtém todos os pontos de extremidade da nuvem contidos no grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="9cd35-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="9cd35-114">Especifique-CloudEndpointName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="9cd35-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="9cd35-115">OS</span><span class="sxs-lookup"><span data-stu-id="9cd35-115">PARAMETERS</span></span>

### <span data-ttu-id="9cd35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd35-116">-DefaultProfile</span></span>
<span data-ttu-id="9cd35-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd35-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd35-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9cd35-118">-Name</span></span>
<span data-ttu-id="9cd35-119">Nome do CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9cd35-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="9cd35-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9cd35-120">-ParentObject</span></span>
<span data-ttu-id="9cd35-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9cd35-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9cd35-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9cd35-122">-ParentResourceId</span></span>
<span data-ttu-id="9cd35-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9cd35-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9cd35-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd35-124">-ResourceGroupName</span></span>
<span data-ttu-id="9cd35-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9cd35-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9cd35-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9cd35-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="9cd35-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="9cd35-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9cd35-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd35-128">-SyncGroupName</span></span>
<span data-ttu-id="9cd35-129">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="9cd35-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="9cd35-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd35-130">CommonParameters</span></span>
<span data-ttu-id="9cd35-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd35-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd35-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd35-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd35-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9cd35-133">INPUTS</span></span>

### <span data-ttu-id="9cd35-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd35-134">System.String</span></span>

### <span data-ttu-id="9cd35-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9cd35-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="9cd35-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9cd35-136">OUTPUTS</span></span>

### <span data-ttu-id="9cd35-137">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cd35-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="9cd35-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9cd35-138">NOTES</span></span>

## <span data-ttu-id="9cd35-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cd35-139">RELATED LINKS</span></span>
