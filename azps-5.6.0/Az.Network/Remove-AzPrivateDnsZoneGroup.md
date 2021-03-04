---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: ada7faf13457f2c074a15b6e409e31afb93ac900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890743"
---
# <span data-ttu-id="2c637-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="2c637-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="2c637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c637-102">SYNOPSIS</span></span>
<span data-ttu-id="2c637-103">Remove um grupo de zonas DNS.</span><span class="sxs-lookup"><span data-stu-id="2c637-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="2c637-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2c637-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c637-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2c637-105">DESCRIPTION</span></span>
<span data-ttu-id="2c637-106">O cmdlet **Remove-AzPrivateDnsZoneGroup** remove um grupo de zonas DNS.</span><span class="sxs-lookup"><span data-stu-id="2c637-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="2c637-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c637-107">EXAMPLES</span></span>

### <span data-ttu-id="2c637-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c637-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="2c637-109">Exemplo acima remove uma zona DNS chamada dnsgroup1 do ponto de extremidade test-pr-endpoint.</span><span class="sxs-lookup"><span data-stu-id="2c637-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="2c637-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2c637-110">PARAMETERS</span></span>

### <span data-ttu-id="2c637-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c637-111">-AsJob</span></span>
<span data-ttu-id="2c637-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2c637-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c637-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c637-113">-DefaultProfile</span></span>
<span data-ttu-id="2c637-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c637-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c637-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2c637-115">-Force</span></span>
<span data-ttu-id="2c637-116">Não peça confirmação se você deseja excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="2c637-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="2c637-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2c637-117">-Name</span></span>
<span data-ttu-id="2c637-118">O nome do grupo de zona dns privado.</span><span class="sxs-lookup"><span data-stu-id="2c637-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c637-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c637-119">-PassThru</span></span>
<span data-ttu-id="2c637-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2c637-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2c637-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="2c637-121">-PrivateEndpointName</span></span>
<span data-ttu-id="2c637-122">O nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="2c637-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="2c637-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c637-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c637-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c637-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2c637-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c637-125">-Confirm</span></span>
<span data-ttu-id="2c637-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c637-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c637-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c637-127">-WhatIf</span></span>
<span data-ttu-id="2c637-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c637-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c637-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c637-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c637-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c637-130">CommonParameters</span></span>
<span data-ttu-id="2c637-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c637-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c637-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c637-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c637-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c637-133">INPUTS</span></span>

### <span data-ttu-id="2c637-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2c637-134">System.String</span></span>

## <span data-ttu-id="2c637-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2c637-135">OUTPUTS</span></span>

### <span data-ttu-id="2c637-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c637-136">System.Boolean</span></span>

## <span data-ttu-id="2c637-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="2c637-137">NOTES</span></span>

## <span data-ttu-id="2c637-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c637-138">RELATED LINKS</span></span>
