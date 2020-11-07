---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 1f6692067c48cc093e7d74d75c678374aba30f24
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774034"
---
# <span data-ttu-id="24e28-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e28-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="24e28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24e28-102">SYNOPSIS</span></span>
<span data-ttu-id="24e28-103">Esse comando lista todos os pontos de extremidade do servidor dentro de um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="24e28-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="24e28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24e28-104">SYNTAX</span></span>

### <span data-ttu-id="24e28-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="24e28-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24e28-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="24e28-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24e28-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="24e28-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24e28-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24e28-108">DESCRIPTION</span></span>
<span data-ttu-id="24e28-109">Esse comando lista todos os pontos de extremidade do servidor dentro de um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="24e28-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="24e28-110">Ele também pode ser usado para listar os atributos de cada ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="24e28-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="24e28-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24e28-111">EXAMPLES</span></span>

### <span data-ttu-id="24e28-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24e28-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="24e28-113">Esse comando obtém todos os pontos de extremidade do servidor contidos no grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="24e28-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="24e28-114">Especifique-ServerEndpointName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="24e28-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="24e28-115">OS</span><span class="sxs-lookup"><span data-stu-id="24e28-115">PARAMETERS</span></span>

### <span data-ttu-id="24e28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e28-116">-DefaultProfile</span></span>
<span data-ttu-id="24e28-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24e28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24e28-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="24e28-118">-Name</span></span>
<span data-ttu-id="24e28-119">Nome do ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="24e28-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="24e28-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24e28-120">-ParentObject</span></span>
<span data-ttu-id="24e28-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="24e28-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="24e28-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="24e28-122">-ParentResourceId</span></span>
<span data-ttu-id="24e28-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="24e28-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="24e28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e28-124">-ResourceGroupName</span></span>
<span data-ttu-id="24e28-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24e28-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="24e28-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="24e28-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="24e28-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="24e28-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="24e28-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="24e28-128">-SyncGroupName</span></span>
<span data-ttu-id="24e28-129">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="24e28-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="24e28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e28-130">CommonParameters</span></span>
<span data-ttu-id="24e28-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e28-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e28-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e28-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24e28-133">INPUTS</span></span>

### <span data-ttu-id="24e28-134">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="24e28-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="24e28-135">System. String</span><span class="sxs-lookup"><span data-stu-id="24e28-135">System.String</span></span>

## <span data-ttu-id="24e28-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24e28-136">OUTPUTS</span></span>

### <span data-ttu-id="24e28-137">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e28-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="24e28-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24e28-138">NOTES</span></span>

## <span data-ttu-id="24e28-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24e28-139">RELATED LINKS</span></span>