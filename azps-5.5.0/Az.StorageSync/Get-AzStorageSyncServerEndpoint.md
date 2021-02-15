---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112490"
---
# <span data-ttu-id="153f4-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="153f4-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="153f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="153f4-102">SYNOPSIS</span></span>
<span data-ttu-id="153f4-103">Esse comando lista todos os pontos de extremidade do servidor dentro de um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="153f4-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="153f4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="153f4-104">SYNTAX</span></span>

### <span data-ttu-id="153f4-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="153f4-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="153f4-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="153f4-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="153f4-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="153f4-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="153f4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="153f4-108">DESCRIPTION</span></span>
<span data-ttu-id="153f4-109">Esse comando lista todos os pontos de extremidade do servidor dentro de um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="153f4-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="153f4-110">Ele também pode ser usado para listar os atributos de cada ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="153f4-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="153f4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="153f4-111">EXAMPLES</span></span>

### <span data-ttu-id="153f4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="153f4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="153f4-113">Esse comando obtém todos os pontos de extremidade do servidor contidos no grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="153f4-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="153f4-114">Especifique -ServerEndpointName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="153f4-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="153f4-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="153f4-115">PARAMETERS</span></span>

### <span data-ttu-id="153f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="153f4-116">-DefaultProfile</span></span>
<span data-ttu-id="153f4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="153f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="153f4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="153f4-118">-Name</span></span>
<span data-ttu-id="153f4-119">Nome do ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="153f4-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="153f4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="153f4-120">-ParentObject</span></span>
<span data-ttu-id="153f4-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="153f4-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="153f4-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="153f4-122">-ParentResourceId</span></span>
<span data-ttu-id="153f4-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="153f4-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="153f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="153f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="153f4-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="153f4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="153f4-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="153f4-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="153f4-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="153f4-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="153f4-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="153f4-128">-SyncGroupName</span></span>
<span data-ttu-id="153f4-129">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="153f4-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="153f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153f4-130">CommonParameters</span></span>
<span data-ttu-id="153f4-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="153f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153f4-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="153f4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153f4-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="153f4-133">INPUTS</span></span>

### <span data-ttu-id="153f4-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="153f4-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="153f4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="153f4-135">System.String</span></span>

## <span data-ttu-id="153f4-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="153f4-136">OUTPUTS</span></span>

### <span data-ttu-id="153f4-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="153f4-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="153f4-138">Notas</span><span class="sxs-lookup"><span data-stu-id="153f4-138">NOTES</span></span>

## <span data-ttu-id="153f4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="153f4-139">RELATED LINKS</span></span>
