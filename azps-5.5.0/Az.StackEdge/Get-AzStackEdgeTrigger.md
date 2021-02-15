---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112525"
---
# <span data-ttu-id="75c0b-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="75c0b-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="75c0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="75c0b-103">Configurar os Gatilhos em um dispositivo</span><span class="sxs-lookup"><span data-stu-id="75c0b-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="75c0b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75c0b-104">SYNTAX</span></span>

### <span data-ttu-id="75c0b-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75c0b-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75c0b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c0b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75c0b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c0b-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75c0b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c0b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="75c0b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="75c0b-109">DESCRIPTION</span></span>
<span data-ttu-id="75c0b-110">O cmdlet **Get-AzStackEdgeTriger** obtém os gatilhos de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75c0b-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="75c0b-111">Você pode especificar o nome como um parâmetro no cmdlet para buscar os detalhes de um Gatilho específico</span><span class="sxs-lookup"><span data-stu-id="75c0b-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="75c0b-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75c0b-112">EXAMPLES</span></span>

### <span data-ttu-id="75c0b-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75c0b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="75c0b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75c0b-114">PARAMETERS</span></span>

### <span data-ttu-id="75c0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c0b-115">-DefaultProfile</span></span>
<span data-ttu-id="75c0b-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75c0b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75c0b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="75c0b-117">-DeviceName</span></span>
<span data-ttu-id="75c0b-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="75c0b-118">Device Name</span></span>

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

### <span data-ttu-id="75c0b-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="75c0b-119">-DeviceObject</span></span>
<span data-ttu-id="75c0b-120">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="75c0b-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="75c0b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="75c0b-121">-Name</span></span>
<span data-ttu-id="75c0b-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="75c0b-122">Resource Name</span></span>

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

### <span data-ttu-id="75c0b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c0b-123">-ResourceGroupName</span></span>
<span data-ttu-id="75c0b-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="75c0b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="75c0b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75c0b-125">-ResourceId</span></span>
<span data-ttu-id="75c0b-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="75c0b-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="75c0b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c0b-127">CommonParameters</span></span>
<span data-ttu-id="75c0b-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c0b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c0b-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75c0b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c0b-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="75c0b-130">INPUTS</span></span>

### <span data-ttu-id="75c0b-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="75c0b-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="75c0b-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="75c0b-132">OUTPUTS</span></span>

### <span data-ttu-id="75c0b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeTri meteor</span><span class="sxs-lookup"><span data-stu-id="75c0b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="75c0b-134">Notas</span><span class="sxs-lookup"><span data-stu-id="75c0b-134">NOTES</span></span>

## <span data-ttu-id="75c0b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75c0b-135">RELATED LINKS</span></span>
