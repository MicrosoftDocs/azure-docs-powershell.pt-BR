---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 81baab4f996d7a56b64f055f94a18c09b4305991
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888029"
---
# <span data-ttu-id="a051e-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a051e-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="a051e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a051e-102">SYNOPSIS</span></span>
<span data-ttu-id="a051e-103">Este comando lista todos os pontos de extremidade do servidor em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a051e-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="a051e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a051e-104">SYNTAX</span></span>

### <span data-ttu-id="a051e-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a051e-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a051e-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a051e-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a051e-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a051e-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a051e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a051e-108">DESCRIPTION</span></span>
<span data-ttu-id="a051e-109">Este comando lista todos os pontos de extremidade do servidor em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a051e-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="a051e-110">Ele também pode ser usado para listar os atributos de cada ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="a051e-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="a051e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a051e-111">EXAMPLES</span></span>

### <span data-ttu-id="a051e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a051e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="a051e-113">Esse comando obtém todos os pontos de extremidade do servidor contidos no grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="a051e-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="a051e-114">Especifique -ServerEndpointName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="a051e-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="a051e-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a051e-115">PARAMETERS</span></span>

### <span data-ttu-id="a051e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a051e-116">-DefaultProfile</span></span>
<span data-ttu-id="a051e-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a051e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a051e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a051e-118">-Name</span></span>
<span data-ttu-id="a051e-119">Nome do ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="a051e-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a051e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a051e-120">-ParentObject</span></span>
<span data-ttu-id="a051e-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a051e-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a051e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a051e-122">-ParentResourceId</span></span>
<span data-ttu-id="a051e-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a051e-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a051e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a051e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a051e-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a051e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a051e-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a051e-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="a051e-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a051e-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a051e-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a051e-128">-SyncGroupName</span></span>
<span data-ttu-id="a051e-129">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="a051e-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a051e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a051e-130">CommonParameters</span></span>
<span data-ttu-id="a051e-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a051e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a051e-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a051e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a051e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a051e-133">INPUTS</span></span>

### <span data-ttu-id="a051e-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a051e-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="a051e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a051e-135">System.String</span></span>

## <span data-ttu-id="a051e-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a051e-136">OUTPUTS</span></span>

### <span data-ttu-id="a051e-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a051e-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a051e-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="a051e-138">NOTES</span></span>

## <span data-ttu-id="a051e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a051e-139">RELATED LINKS</span></span>
