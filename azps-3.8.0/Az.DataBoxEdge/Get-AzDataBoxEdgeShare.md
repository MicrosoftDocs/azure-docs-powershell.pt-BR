---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943416"
---
# <span data-ttu-id="50be6-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="50be6-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="50be6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50be6-102">SYNOPSIS</span></span>
<span data-ttu-id="50be6-103">Obtém os compartilhamentos disponíveis para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50be6-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="50be6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50be6-104">SYNTAX</span></span>

### <span data-ttu-id="50be6-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="50be6-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50be6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50be6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50be6-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50be6-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50be6-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50be6-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="50be6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50be6-109">DESCRIPTION</span></span>
<span data-ttu-id="50be6-110">O cmdlet **Get-AzDataBoxEdgeShare** Obtém os compartilhamentos disponíveis para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="50be6-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="50be6-111">Se o nome for fornecido, você receberá o compartilhamento por nome.</span><span class="sxs-lookup"><span data-stu-id="50be6-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="50be6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50be6-112">EXAMPLES</span></span>

### <span data-ttu-id="50be6-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50be6-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="50be6-114">OS</span><span class="sxs-lookup"><span data-stu-id="50be6-114">PARAMETERS</span></span>

### <span data-ttu-id="50be6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50be6-115">-DefaultProfile</span></span>
<span data-ttu-id="50be6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50be6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50be6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="50be6-117">-DeviceName</span></span>
<span data-ttu-id="50be6-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="50be6-118">Device Name</span></span>

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

### <span data-ttu-id="50be6-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="50be6-119">-DeviceObject</span></span>
<span data-ttu-id="50be6-120">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="50be6-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="50be6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="50be6-121">-Name</span></span>
<span data-ttu-id="50be6-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="50be6-122">Resource Name</span></span>

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

### <span data-ttu-id="50be6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50be6-123">-ResourceGroupName</span></span>
<span data-ttu-id="50be6-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="50be6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="50be6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50be6-125">-ResourceId</span></span>
<span data-ttu-id="50be6-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="50be6-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="50be6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50be6-127">CommonParameters</span></span>
<span data-ttu-id="50be6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50be6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50be6-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50be6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50be6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50be6-130">INPUTS</span></span>

### <span data-ttu-id="50be6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="50be6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="50be6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50be6-132">OUTPUTS</span></span>

### <span data-ttu-id="50be6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="50be6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="50be6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50be6-134">NOTES</span></span>

## <span data-ttu-id="50be6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50be6-135">RELATED LINKS</span></span>
