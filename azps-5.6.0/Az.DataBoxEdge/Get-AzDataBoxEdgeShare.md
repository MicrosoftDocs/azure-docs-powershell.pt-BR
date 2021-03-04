---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 616830906621b673010ca8708b909608c06f93fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891469"
---
# <span data-ttu-id="519b0-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="519b0-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="519b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="519b0-102">SYNOPSIS</span></span>
<span data-ttu-id="519b0-103">Obtém os compartilhamentos disponíveis para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="519b0-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="519b0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="519b0-104">SYNTAX</span></span>

### <span data-ttu-id="519b0-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="519b0-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="519b0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="519b0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="519b0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="519b0-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="519b0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="519b0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="519b0-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="519b0-109">DESCRIPTION</span></span>
<span data-ttu-id="519b0-110">O cmdlet **Get-AzDataBoxEdgeShare** obtém os compartilhamentos disponíveis para um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="519b0-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="519b0-111">Se Name for fornecido, ele receberá o compartilhamento por Nome.</span><span class="sxs-lookup"><span data-stu-id="519b0-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="519b0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="519b0-112">EXAMPLES</span></span>

### <span data-ttu-id="519b0-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="519b0-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="519b0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="519b0-114">PARAMETERS</span></span>

### <span data-ttu-id="519b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="519b0-115">-DefaultProfile</span></span>
<span data-ttu-id="519b0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="519b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="519b0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="519b0-117">-DeviceName</span></span>
<span data-ttu-id="519b0-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="519b0-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519b0-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="519b0-119">-DeviceObject</span></span>
<span data-ttu-id="519b0-120">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="519b0-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="519b0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="519b0-121">-Name</span></span>
<span data-ttu-id="519b0-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="519b0-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="519b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="519b0-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="519b0-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519b0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="519b0-125">-ResourceId</span></span>
<span data-ttu-id="519b0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="519b0-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519b0-127">CommonParameters</span></span>
<span data-ttu-id="519b0-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="519b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="519b0-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="519b0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519b0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="519b0-130">INPUTS</span></span>

### <span data-ttu-id="519b0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="519b0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="519b0-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="519b0-132">OUTPUTS</span></span>

### <span data-ttu-id="519b0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="519b0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="519b0-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="519b0-134">NOTES</span></span>

## <span data-ttu-id="519b0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="519b0-135">RELATED LINKS</span></span>
