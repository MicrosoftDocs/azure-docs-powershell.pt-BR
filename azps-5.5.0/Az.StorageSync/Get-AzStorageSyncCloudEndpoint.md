---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112497"
---
# <span data-ttu-id="5be9f-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be9f-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="5be9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5be9f-102">SYNOPSIS</span></span>
<span data-ttu-id="5be9f-103">Esse comando lista todos os pontos de extremidade de nuvem dentro de um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="5be9f-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="5be9f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5be9f-104">SYNTAX</span></span>

### <span data-ttu-id="5be9f-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5be9f-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5be9f-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5be9f-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5be9f-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5be9f-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5be9f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5be9f-108">DESCRIPTION</span></span>
<span data-ttu-id="5be9f-109">Esse comando lista todos os pontos de extremidade de nuvem dentro de um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="5be9f-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="5be9f-110">Ele também pode ser usado para listar os atributos de cada ponto de extremidade de nuvem.</span><span class="sxs-lookup"><span data-stu-id="5be9f-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="5be9f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5be9f-111">EXAMPLES</span></span>

### <span data-ttu-id="5be9f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5be9f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="5be9f-113">Esse comando obtém todos os pontos de extremidade de nuvem contidos no grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="5be9f-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="5be9f-114">Especifique -CloudEndpointName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="5be9f-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="5be9f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5be9f-115">PARAMETERS</span></span>

### <span data-ttu-id="5be9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be9f-116">-DefaultProfile</span></span>
<span data-ttu-id="5be9f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5be9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5be9f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5be9f-118">-Name</span></span>
<span data-ttu-id="5be9f-119">Nome do CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5be9f-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="5be9f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5be9f-120">-ParentObject</span></span>
<span data-ttu-id="5be9f-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5be9f-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="5be9f-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5be9f-122">-ParentResourceId</span></span>
<span data-ttu-id="5be9f-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5be9f-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="5be9f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be9f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5be9f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5be9f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="5be9f-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5be9f-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="5be9f-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5be9f-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="5be9f-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5be9f-128">-SyncGroupName</span></span>
<span data-ttu-id="5be9f-129">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="5be9f-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="5be9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be9f-130">CommonParameters</span></span>
<span data-ttu-id="5be9f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5be9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be9f-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5be9f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be9f-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="5be9f-133">INPUTS</span></span>

### <span data-ttu-id="5be9f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5be9f-134">System.String</span></span>

### <span data-ttu-id="5be9f-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5be9f-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="5be9f-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="5be9f-136">OUTPUTS</span></span>

### <span data-ttu-id="5be9f-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be9f-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="5be9f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="5be9f-138">NOTES</span></span>

## <span data-ttu-id="5be9f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5be9f-139">RELATED LINKS</span></span>
