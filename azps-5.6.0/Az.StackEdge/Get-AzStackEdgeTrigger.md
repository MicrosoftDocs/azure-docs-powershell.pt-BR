---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: a4bcbad5f595efe126ed232b94d5deb368515bc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888416"
---
# <span data-ttu-id="e29df-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="e29df-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="e29df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29df-102">SYNOPSIS</span></span>
<span data-ttu-id="e29df-103">Obter os Gatilhos configurados em um dispositivo</span><span class="sxs-lookup"><span data-stu-id="e29df-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="e29df-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e29df-104">SYNTAX</span></span>

### <span data-ttu-id="e29df-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e29df-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e29df-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e29df-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e29df-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e29df-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e29df-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e29df-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e29df-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e29df-109">DESCRIPTION</span></span>
<span data-ttu-id="e29df-110">O cmdlet **Get-AzStackEdgeTriger** obtém os gatilhos de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e29df-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="e29df-111">Você pode especificar o nome como um parâmetro no cmdlet para buscar os detalhes de um Triggers específicos</span><span class="sxs-lookup"><span data-stu-id="e29df-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="e29df-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e29df-112">EXAMPLES</span></span>

### <span data-ttu-id="e29df-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e29df-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="e29df-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e29df-114">PARAMETERS</span></span>

### <span data-ttu-id="e29df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29df-115">-DefaultProfile</span></span>
<span data-ttu-id="e29df-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e29df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e29df-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e29df-117">-DeviceName</span></span>
<span data-ttu-id="e29df-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e29df-118">Device Name</span></span>

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

### <span data-ttu-id="e29df-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e29df-119">-DeviceObject</span></span>
<span data-ttu-id="e29df-120">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="e29df-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e29df-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e29df-121">-Name</span></span>
<span data-ttu-id="e29df-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="e29df-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e29df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29df-123">-ResourceGroupName</span></span>
<span data-ttu-id="e29df-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e29df-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e29df-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e29df-125">-ResourceId</span></span>
<span data-ttu-id="e29df-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e29df-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="e29df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29df-127">CommonParameters</span></span>
<span data-ttu-id="e29df-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29df-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e29df-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29df-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e29df-130">INPUTS</span></span>

### <span data-ttu-id="e29df-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e29df-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="e29df-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e29df-132">OUTPUTS</span></span>

### <span data-ttu-id="e29df-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="e29df-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="e29df-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="e29df-134">NOTES</span></span>

## <span data-ttu-id="e29df-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e29df-135">RELATED LINKS</span></span>
