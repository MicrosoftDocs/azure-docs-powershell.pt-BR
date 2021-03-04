---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 71540063e9eb4323d94a579df8f6489719f7c3fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893082"
---
# <span data-ttu-id="8f380-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8f380-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="8f380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f380-102">SYNOPSIS</span></span>
<span data-ttu-id="8f380-103">Obtém os contêineres de uma conta de Armazenamento de Borda em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f380-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="8f380-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8f380-104">SYNTAX</span></span>

### <span data-ttu-id="8f380-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f380-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f380-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f380-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f380-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f380-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f380-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f380-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="8f380-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8f380-109">DESCRIPTION</span></span>
<span data-ttu-id="8f380-110">O cmdlet **Get-AzStackEdgeStorageContainer** obtém o contêiner de armazenamento de uma conta de Armazenamento de Borda em um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="8f380-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="8f380-111">Você pode especificar o nome como um parâmetro no cmdlet para buscar os detalhes de um contêiner de armazenamento específico.</span><span class="sxs-lookup"><span data-stu-id="8f380-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="8f380-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f380-112">EXAMPLES</span></span>

### <span data-ttu-id="8f380-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f380-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="8f380-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8f380-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="8f380-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8f380-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="8f380-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8f380-116">PARAMETERS</span></span>

### <span data-ttu-id="8f380-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f380-117">-DefaultProfile</span></span>
<span data-ttu-id="8f380-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f380-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f380-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8f380-119">-DeviceName</span></span>
<span data-ttu-id="8f380-120">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8f380-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f380-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8f380-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="8f380-122">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="8f380-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f380-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="8f380-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="8f380-124">Fornecer objeto EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="8f380-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f380-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8f380-125">-Name</span></span>
<span data-ttu-id="8f380-126">Nome do EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8f380-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f380-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f380-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f380-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8f380-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f380-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f380-129">-ResourceId</span></span>
<span data-ttu-id="8f380-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f380-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f380-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f380-131">CommonParameters</span></span>
<span data-ttu-id="8f380-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f380-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f380-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f380-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f380-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f380-134">INPUTS</span></span>

### <span data-ttu-id="8f380-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8f380-135">System.String</span></span>

### <span data-ttu-id="8f380-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8f380-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8f380-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8f380-137">OUTPUTS</span></span>

### <span data-ttu-id="8f380-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8f380-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="8f380-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="8f380-139">NOTES</span></span>

## <span data-ttu-id="8f380-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f380-140">RELATED LINKS</span></span>
