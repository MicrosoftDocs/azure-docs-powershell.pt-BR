---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113943"
---
# <span data-ttu-id="ff306-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ff306-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="ff306-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff306-102">SYNOPSIS</span></span>
<span data-ttu-id="ff306-103">Obtém os compartilhamentos disponíveis para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff306-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="ff306-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff306-104">SYNTAX</span></span>

### <span data-ttu-id="ff306-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ff306-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff306-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff306-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff306-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff306-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff306-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff306-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ff306-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff306-109">DESCRIPTION</span></span>
<span data-ttu-id="ff306-110">O cmdlet **Get-AzSt stackEdgeShare** obtém os compartilhamentos disponíveis para um dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="ff306-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="ff306-111">Se o Nome for fornecido, isso receberá o compartilhamento por Nome.</span><span class="sxs-lookup"><span data-stu-id="ff306-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="ff306-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff306-112">EXAMPLES</span></span>

### <span data-ttu-id="ff306-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ff306-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="ff306-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff306-114">PARAMETERS</span></span>

### <span data-ttu-id="ff306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff306-115">-DefaultProfile</span></span>
<span data-ttu-id="ff306-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff306-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff306-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ff306-117">-DeviceName</span></span>
<span data-ttu-id="ff306-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ff306-118">Device Name</span></span>

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

### <span data-ttu-id="ff306-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ff306-119">-DeviceObject</span></span>
<span data-ttu-id="ff306-120">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="ff306-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff306-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff306-121">-Name</span></span>
<span data-ttu-id="ff306-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="ff306-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff306-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff306-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff306-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ff306-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ff306-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff306-125">-ResourceId</span></span>
<span data-ttu-id="ff306-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff306-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff306-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff306-127">CommonParameters</span></span>
<span data-ttu-id="ff306-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff306-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff306-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff306-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff306-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="ff306-130">INPUTS</span></span>

### <span data-ttu-id="ff306-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ff306-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ff306-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="ff306-132">OUTPUTS</span></span>

### <span data-ttu-id="ff306-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ff306-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="ff306-134">Notas</span><span class="sxs-lookup"><span data-stu-id="ff306-134">NOTES</span></span>

## <span data-ttu-id="ff306-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff306-135">RELATED LINKS</span></span>
