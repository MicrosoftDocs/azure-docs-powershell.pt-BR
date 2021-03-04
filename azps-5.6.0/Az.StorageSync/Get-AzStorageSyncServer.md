---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: 525d51d62477db88da78eaecc482d6cf64dbf810
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888030"
---
# <span data-ttu-id="cb832-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="cb832-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="cb832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb832-102">SYNOPSIS</span></span>
<span data-ttu-id="cb832-103">Este comando lista todos os servidores registrados em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cb832-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="cb832-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cb832-104">SYNTAX</span></span>

### <span data-ttu-id="cb832-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cb832-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb832-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb832-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb832-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb832-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb832-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cb832-108">DESCRIPTION</span></span>
<span data-ttu-id="cb832-109">Este comando lista todos os servidores registrados em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cb832-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="cb832-110">Ele também pode ser usado para listar os atributos de cada servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="cb832-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="cb832-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb832-111">EXAMPLES</span></span>

### <span data-ttu-id="cb832-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cb832-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="cb832-113">Esse comando obtém todos os servidores registrados em um serviço de sincronização de armazenamento específico.</span><span class="sxs-lookup"><span data-stu-id="cb832-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="cb832-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cb832-114">PARAMETERS</span></span>

### <span data-ttu-id="cb832-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb832-115">-DefaultProfile</span></span>
<span data-ttu-id="cb832-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb832-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb832-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cb832-117">-ParentObject</span></span>
<span data-ttu-id="cb832-118">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cb832-118">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb832-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cb832-119">-ParentResourceId</span></span>
<span data-ttu-id="cb832-120">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cb832-120">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb832-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb832-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb832-122">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="cb832-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb832-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="cb832-123">-ServerId</span></span>
<span data-ttu-id="cb832-124">Nome do RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="cb832-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb832-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="cb832-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="cb832-126">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="cb832-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="cb832-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb832-127">CommonParameters</span></span>
<span data-ttu-id="cb832-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb832-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb832-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb832-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb832-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb832-130">INPUTS</span></span>

### <span data-ttu-id="cb832-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cb832-131">System.String</span></span>

### <span data-ttu-id="cb832-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="cb832-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="cb832-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cb832-133">System.Guid</span></span>

## <span data-ttu-id="cb832-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cb832-134">OUTPUTS</span></span>

### <span data-ttu-id="cb832-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="cb832-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="cb832-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="cb832-136">NOTES</span></span>

## <span data-ttu-id="cb832-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb832-137">RELATED LINKS</span></span>
