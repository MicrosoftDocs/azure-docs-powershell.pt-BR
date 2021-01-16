---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: fef6f1615bb2e3dd9d3bb19738ea6cef393235aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260695"
---
# <span data-ttu-id="f2caf-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="f2caf-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="f2caf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2caf-102">SYNOPSIS</span></span>
<span data-ttu-id="f2caf-103">Obtém uma lista de prefixos de serviço de emparelhamento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f2caf-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="f2caf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2caf-104">SYNTAX</span></span>

### <span data-ttu-id="f2caf-105">ByResourceGroupAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2caf-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2caf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f2caf-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2caf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2caf-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2caf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2caf-108">DESCRIPTION</span></span>
<span data-ttu-id="f2caf-109">Listar prefixos do serviço de emparelhamento para objetos de serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="f2caf-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="f2caf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2caf-110">EXAMPLES</span></span>

### <span data-ttu-id="f2caf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2caf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="f2caf-112">Obtém os prefixos para um serviço de emparelhamento com base em comandos de tubulação.</span><span class="sxs-lookup"><span data-stu-id="f2caf-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="f2caf-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f2caf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="f2caf-114">Obtém um prefixo específico para um serviço de emparelhamento por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f2caf-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="f2caf-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f2caf-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="f2caf-116">Obtém um prefixo específico para um serviço de emparelhamento por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f2caf-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="f2caf-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="f2caf-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="f2caf-118">Obtém um prefixo específico para um serviço de emparelhamento com atributos expandidos</span><span class="sxs-lookup"><span data-stu-id="f2caf-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="f2caf-119">OS</span><span class="sxs-lookup"><span data-stu-id="f2caf-119">PARAMETERS</span></span>

### <span data-ttu-id="f2caf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2caf-120">-DefaultProfile</span></span>
<span data-ttu-id="f2caf-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2caf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2caf-122">-Expandir</span><span class="sxs-lookup"><span data-stu-id="f2caf-122">-Expand</span></span>
<span data-ttu-id="f2caf-123">Exibir os eventos para um prefixo de serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="f2caf-123">View the events for a peering service prefix</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2caf-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2caf-124">-Name</span></span>
<span data-ttu-id="f2caf-125">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f2caf-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2caf-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="f2caf-126">-PeeringServiceName</span></span>
<span data-ttu-id="f2caf-127">O nome do serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f2caf-127">The peering service name.</span></span> <span data-ttu-id="f2caf-128">Use New-AzPeeringService cmdlet para um novo serviço de emparelhamento ou Get-AzPeeringService para obter uma lista.</span><span class="sxs-lookup"><span data-stu-id="f2caf-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2caf-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="f2caf-129">-PeeringServiceObject</span></span>
<span data-ttu-id="f2caf-130">Usar uma Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="f2caf-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2caf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2caf-131">-ResourceGroupName</span></span>
<span data-ttu-id="f2caf-132">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="f2caf-132">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2caf-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2caf-133">-ResourceId</span></span>
<span data-ttu-id="f2caf-134">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f2caf-134">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2caf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2caf-135">CommonParameters</span></span>
<span data-ttu-id="f2caf-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2caf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2caf-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2caf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2caf-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2caf-138">INPUTS</span></span>

### <span data-ttu-id="f2caf-139">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="f2caf-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="f2caf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f2caf-140">System.String</span></span>

## <span data-ttu-id="f2caf-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2caf-141">OUTPUTS</span></span>

### <span data-ttu-id="f2caf-142">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="f2caf-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="f2caf-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2caf-143">NOTES</span></span>

## <span data-ttu-id="f2caf-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2caf-144">RELATED LINKS</span></span>
