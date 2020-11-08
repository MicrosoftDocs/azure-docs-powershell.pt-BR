---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116631"
---
# <span data-ttu-id="db67e-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="db67e-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="db67e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db67e-102">SYNOPSIS</span></span>
<span data-ttu-id="db67e-103">Obter os gatilhos configurados em um dispositivo</span><span class="sxs-lookup"><span data-stu-id="db67e-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="db67e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db67e-104">SYNTAX</span></span>

### <span data-ttu-id="db67e-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="db67e-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db67e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db67e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db67e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db67e-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db67e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db67e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="db67e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db67e-109">DESCRIPTION</span></span>
<span data-ttu-id="db67e-110">O cmdlet **Get-AzStackEdgeTriger** Obtém os gatilhos de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db67e-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="db67e-111">Você pode especificar o nome como um parâmetro no cmdlet para buscar os detalhes de um gatilho específico específico</span><span class="sxs-lookup"><span data-stu-id="db67e-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="db67e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db67e-112">EXAMPLES</span></span>

### <span data-ttu-id="db67e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db67e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="db67e-114">OS</span><span class="sxs-lookup"><span data-stu-id="db67e-114">PARAMETERS</span></span>

### <span data-ttu-id="db67e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db67e-115">-DefaultProfile</span></span>
<span data-ttu-id="db67e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db67e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db67e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="db67e-117">-DeviceName</span></span>
<span data-ttu-id="db67e-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="db67e-118">Device Name</span></span>

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

### <span data-ttu-id="db67e-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="db67e-119">-DeviceObject</span></span>
<span data-ttu-id="db67e-120">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="db67e-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="db67e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="db67e-121">-Name</span></span>
<span data-ttu-id="db67e-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="db67e-122">Resource Name</span></span>

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

### <span data-ttu-id="db67e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db67e-123">-ResourceGroupName</span></span>
<span data-ttu-id="db67e-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="db67e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="db67e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db67e-125">-ResourceId</span></span>
<span data-ttu-id="db67e-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="db67e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="db67e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db67e-127">CommonParameters</span></span>
<span data-ttu-id="db67e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db67e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db67e-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db67e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db67e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db67e-130">INPUTS</span></span>

### <span data-ttu-id="db67e-131">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="db67e-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="db67e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db67e-132">OUTPUTS</span></span>

### <span data-ttu-id="db67e-133">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="db67e-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="db67e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db67e-134">NOTES</span></span>

## <span data-ttu-id="db67e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db67e-135">RELATED LINKS</span></span>
