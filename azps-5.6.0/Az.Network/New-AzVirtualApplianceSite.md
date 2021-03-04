---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: e27d956f8530fb45f5927ece22302d21acafc503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886433"
---
# <span data-ttu-id="4237f-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4237f-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="4237f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4237f-102">SYNOPSIS</span></span>
<span data-ttu-id="4237f-103">Crie um site conectado a um Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="4237f-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="4237f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4237f-104">SYNTAX</span></span>

### <span data-ttu-id="4237f-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4237f-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4237f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4237f-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4237f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4237f-107">DESCRIPTION</span></span>
<span data-ttu-id="4237f-108">O New-AzVirtualApplianceSite cria um site de Dispositivo Virtual conectado a um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="4237f-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="4237f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4237f-109">EXAMPLES</span></span>

### <span data-ttu-id="4237f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4237f-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="4237f-111">Crie um novo site de Dispositivo Virtual no grupo de recursos: testrg.</span><span class="sxs-lookup"><span data-stu-id="4237f-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="4237f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4237f-112">PARAMETERS</span></span>

### <span data-ttu-id="4237f-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4237f-113">-AddressPrefix</span></span>
<span data-ttu-id="4237f-114">O prefixo de endereço do site.</span><span class="sxs-lookup"><span data-stu-id="4237f-114">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4237f-115">-AsJob</span></span>
<span data-ttu-id="4237f-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4237f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4237f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4237f-117">-DefaultProfile</span></span>
<span data-ttu-id="4237f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4237f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4237f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4237f-119">-Force</span></span>
<span data-ttu-id="4237f-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="4237f-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4237f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4237f-121">-Name</span></span>
<span data-ttu-id="4237f-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4237f-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="4237f-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="4237f-124">O dispositivo virtual de rede ao que este site está anexado.</span><span class="sxs-lookup"><span data-stu-id="4237f-124">The Network virtual appliance that this site is attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="4237f-125">-O365Policy</span></span>
<span data-ttu-id="4237f-126">A política de quebra do Office 365.</span><span class="sxs-lookup"><span data-stu-id="4237f-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4237f-127">-ResourceGroupName</span></span>
<span data-ttu-id="4237f-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4237f-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4237f-129">-ResourceId</span></span>
<span data-ttu-id="4237f-130">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="4237f-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4237f-131">-Tag</span></span>
<span data-ttu-id="4237f-132">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="4237f-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4237f-133">-Confirm</span></span>
<span data-ttu-id="4237f-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4237f-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4237f-135">-WhatIf</span></span>
<span data-ttu-id="4237f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4237f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4237f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4237f-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4237f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4237f-138">CommonParameters</span></span>
<span data-ttu-id="4237f-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4237f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4237f-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4237f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4237f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4237f-141">INPUTS</span></span>

### <span data-ttu-id="4237f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4237f-142">System.String</span></span>

### <span data-ttu-id="4237f-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="4237f-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="4237f-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4237f-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4237f-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4237f-145">OUTPUTS</span></span>

### <span data-ttu-id="4237f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4237f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="4237f-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="4237f-147">NOTES</span></span>

## <span data-ttu-id="4237f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4237f-148">RELATED LINKS</span></span>
