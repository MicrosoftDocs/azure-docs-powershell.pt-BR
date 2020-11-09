---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284297"
---
# <span data-ttu-id="b9a27-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="b9a27-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="b9a27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9a27-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a27-103">Crie um site conectado a um aplicativo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="b9a27-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="b9a27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9a27-104">SYNTAX</span></span>

### <span data-ttu-id="b9a27-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9a27-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a27-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a27-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a27-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9a27-107">DESCRIPTION</span></span>
<span data-ttu-id="b9a27-108">O comando New-AzVirtualApplianceSite cria um site de dispositivo virtual conectado a um recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="b9a27-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b9a27-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9a27-109">EXAMPLES</span></span>

### <span data-ttu-id="b9a27-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9a27-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="b9a27-111">Crie um novo site de dispositivo virtual no grupo de recursos: testrg.</span><span class="sxs-lookup"><span data-stu-id="b9a27-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="b9a27-112">OS</span><span class="sxs-lookup"><span data-stu-id="b9a27-112">PARAMETERS</span></span>

### <span data-ttu-id="b9a27-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b9a27-113">-AddressPrefix</span></span>
<span data-ttu-id="b9a27-114">O prefixo do endereço do site.</span><span class="sxs-lookup"><span data-stu-id="b9a27-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="b9a27-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9a27-115">-AsJob</span></span>
<span data-ttu-id="b9a27-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b9a27-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9a27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a27-117">-DefaultProfile</span></span>
<span data-ttu-id="b9a27-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a27-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9a27-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b9a27-119">-Force</span></span>
<span data-ttu-id="b9a27-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b9a27-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b9a27-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9a27-121">-Name</span></span>
<span data-ttu-id="b9a27-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9a27-122">The resource name.</span></span>

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

### <span data-ttu-id="b9a27-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="b9a27-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="b9a27-124">O dispositivo de rede virtual ao qual este site está associado.</span><span class="sxs-lookup"><span data-stu-id="b9a27-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="b9a27-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="b9a27-125">-O365Policy</span></span>
<span data-ttu-id="b9a27-126">A política de debates do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b9a27-126">The Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="b9a27-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a27-127">-ResourceGroupName</span></span>
<span data-ttu-id="b9a27-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9a27-128">The resource group name.</span></span>

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

### <span data-ttu-id="b9a27-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9a27-129">-ResourceId</span></span>
<span data-ttu-id="b9a27-130">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9a27-130">The resource id.</span></span>

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

### <span data-ttu-id="b9a27-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="b9a27-131">-Tag</span></span>
<span data-ttu-id="b9a27-132">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9a27-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b9a27-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9a27-133">-Confirm</span></span>
<span data-ttu-id="b9a27-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a27-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a27-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a27-135">-WhatIf</span></span>
<span data-ttu-id="b9a27-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9a27-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a27-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9a27-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a27-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a27-138">CommonParameters</span></span>
<span data-ttu-id="b9a27-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a27-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a27-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9a27-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a27-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9a27-141">INPUTS</span></span>

### <span data-ttu-id="b9a27-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b9a27-142">System.String</span></span>

### <span data-ttu-id="b9a27-143">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="b9a27-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="b9a27-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b9a27-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b9a27-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9a27-145">OUTPUTS</span></span>

### <span data-ttu-id="b9a27-146">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="b9a27-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="b9a27-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9a27-147">NOTES</span></span>

## <span data-ttu-id="b9a27-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9a27-148">RELATED LINKS</span></span>
