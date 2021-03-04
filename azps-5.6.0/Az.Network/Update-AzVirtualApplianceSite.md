---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 7d0d292cb7eba6b776371493e9ceb7e19ef17115
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885336"
---
# <span data-ttu-id="1530f-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="1530f-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="1530f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1530f-102">SYNOPSIS</span></span>
<span data-ttu-id="1530f-103">Alterar ou modificar um site de Dispositivo Virtual conectado a um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="1530f-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1530f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1530f-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1530f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1530f-105">DESCRIPTION</span></span>
<span data-ttu-id="1530f-106">O Update-AzVirtualApplianceSite comando modifica um recurso de site do Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="1530f-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="1530f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1530f-107">EXAMPLES</span></span>

### <span data-ttu-id="1530f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1530f-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="1530f-109">Modifique o prefixo de endereço para um recurso de site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="1530f-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="1530f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1530f-110">PARAMETERS</span></span>

### <span data-ttu-id="1530f-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="1530f-111">-AddresssPrefix</span></span>
<span data-ttu-id="1530f-112">O prefixo de endereço do site.</span><span class="sxs-lookup"><span data-stu-id="1530f-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1530f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1530f-113">-AsJob</span></span>
<span data-ttu-id="1530f-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1530f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1530f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1530f-115">-DefaultProfile</span></span>
<span data-ttu-id="1530f-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1530f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1530f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1530f-117">-Force</span></span>
<span data-ttu-id="1530f-118">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="1530f-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1530f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1530f-119">-Name</span></span>
<span data-ttu-id="1530f-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1530f-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1530f-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="1530f-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="1530f-122">Dispositivo virtual de rede ao que este site está anexado.</span><span class="sxs-lookup"><span data-stu-id="1530f-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="1530f-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="1530f-123">-O365Policy</span></span>
<span data-ttu-id="1530f-124">Política de fuga do Office 365.</span><span class="sxs-lookup"><span data-stu-id="1530f-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1530f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1530f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1530f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1530f-126">The resource group name.</span></span>

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

### <span data-ttu-id="1530f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="1530f-127">-Tag</span></span>
<span data-ttu-id="1530f-128">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="1530f-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1530f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1530f-129">-Confirm</span></span>
<span data-ttu-id="1530f-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1530f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1530f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1530f-131">-WhatIf</span></span>
<span data-ttu-id="1530f-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1530f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1530f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1530f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1530f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1530f-134">CommonParameters</span></span>
<span data-ttu-id="1530f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1530f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1530f-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1530f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1530f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1530f-137">INPUTS</span></span>

### <span data-ttu-id="1530f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1530f-138">System.String</span></span>

### <span data-ttu-id="1530f-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="1530f-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="1530f-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1530f-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1530f-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1530f-141">OUTPUTS</span></span>

### <span data-ttu-id="1530f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="1530f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="1530f-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="1530f-143">NOTES</span></span>

## <span data-ttu-id="1530f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1530f-144">RELATED LINKS</span></span>
