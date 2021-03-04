---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: f5451b2c3af331f0086f39f46028aff1d33bf002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890237"
---
# <span data-ttu-id="94896-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="94896-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="94896-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94896-102">SYNOPSIS</span></span>
<span data-ttu-id="94896-103">Remove um VpnServerConfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="94896-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="94896-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="94896-104">SYNTAX</span></span>

### <span data-ttu-id="94896-105">ByVpnServerConfigurationName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="94896-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94896-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="94896-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94896-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="94896-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94896-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="94896-108">DESCRIPTION</span></span>
<span data-ttu-id="94896-109">{{Preencha a Descrição}}</span><span class="sxs-lookup"><span data-stu-id="94896-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="94896-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94896-110">EXAMPLES</span></span>

### <span data-ttu-id="94896-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="94896-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="94896-112">O comando acima removerá um VpnServerConfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="94896-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="94896-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="94896-113">PARAMETERS</span></span>

### <span data-ttu-id="94896-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94896-114">-DefaultProfile</span></span>
<span data-ttu-id="94896-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94896-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-116">-Force</span><span class="sxs-lookup"><span data-stu-id="94896-116">-Force</span></span>
<span data-ttu-id="94896-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="94896-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94896-118">-InputObject</span></span>
<span data-ttu-id="94896-119">O objeto vpnServerConfiguration a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="94896-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94896-120">-Name</span><span class="sxs-lookup"><span data-stu-id="94896-120">-Name</span></span>
<span data-ttu-id="94896-121">O nome vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="94896-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94896-122">-PassThru</span></span>
<span data-ttu-id="94896-123">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="94896-123">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94896-124">-ResourceGroupName</span></span>
<span data-ttu-id="94896-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94896-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94896-126">-ResourceId</span></span>
<span data-ttu-id="94896-127">A ID de recurso do Azure para o vpnServerConfiguration a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="94896-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94896-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94896-128">-Confirm</span></span>
<span data-ttu-id="94896-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94896-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94896-130">-WhatIf</span></span>
<span data-ttu-id="94896-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94896-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94896-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94896-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94896-133">CommonParameters</span></span>
<span data-ttu-id="94896-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94896-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94896-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94896-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94896-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94896-136">INPUTS</span></span>

### <span data-ttu-id="94896-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="94896-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="94896-138">System.String</span><span class="sxs-lookup"><span data-stu-id="94896-138">System.String</span></span>

## <span data-ttu-id="94896-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="94896-139">OUTPUTS</span></span>

### <span data-ttu-id="94896-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94896-140">System.Boolean</span></span>

## <span data-ttu-id="94896-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="94896-141">NOTES</span></span>

## <span data-ttu-id="94896-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94896-142">RELATED LINKS</span></span>
