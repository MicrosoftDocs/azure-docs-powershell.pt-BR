---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111566"
---
# <span data-ttu-id="abc43-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="abc43-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="abc43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abc43-102">SYNOPSIS</span></span>
<span data-ttu-id="abc43-103">Remove uma configuração VpnServerConfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="abc43-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="abc43-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abc43-104">SYNTAX</span></span>

### <span data-ttu-id="abc43-105">ByVpnServerConfigurationName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="abc43-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc43-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="abc43-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc43-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="abc43-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc43-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="abc43-108">DESCRIPTION</span></span>
<span data-ttu-id="abc43-109">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="abc43-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="abc43-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="abc43-110">EXAMPLES</span></span>

### <span data-ttu-id="abc43-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="abc43-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="abc43-112">O comando acima removerá uma Configuração VpnServer existente.</span><span class="sxs-lookup"><span data-stu-id="abc43-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="abc43-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abc43-113">PARAMETERS</span></span>

### <span data-ttu-id="abc43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc43-114">-DefaultProfile</span></span>
<span data-ttu-id="abc43-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abc43-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abc43-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="abc43-116">-Force</span></span>
<span data-ttu-id="abc43-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="abc43-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="abc43-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abc43-118">-InputObject</span></span>
<span data-ttu-id="abc43-119">O objeto vpnServerConfiguration a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="abc43-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="abc43-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="abc43-120">-Name</span></span>
<span data-ttu-id="abc43-121">O nome vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="abc43-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="abc43-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abc43-122">-PassThru</span></span>
<span data-ttu-id="abc43-123">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="abc43-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="abc43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc43-124">-ResourceGroupName</span></span>
<span data-ttu-id="abc43-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="abc43-125">The resource group name.</span></span>

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

### <span data-ttu-id="abc43-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abc43-126">-ResourceId</span></span>
<span data-ttu-id="abc43-127">A ID de recurso do Azure para que o vpnServerConfiguration seja excluído.</span><span class="sxs-lookup"><span data-stu-id="abc43-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="abc43-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="abc43-128">-Confirm</span></span>
<span data-ttu-id="abc43-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abc43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc43-130">-WhatIf</span></span>
<span data-ttu-id="abc43-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="abc43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc43-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abc43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc43-133">CommonParameters</span></span>
<span data-ttu-id="abc43-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc43-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc43-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc43-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="abc43-136">INPUTS</span></span>

### <span data-ttu-id="abc43-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="abc43-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="abc43-138">System.String</span><span class="sxs-lookup"><span data-stu-id="abc43-138">System.String</span></span>

## <span data-ttu-id="abc43-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="abc43-139">OUTPUTS</span></span>

### <span data-ttu-id="abc43-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="abc43-140">System.Boolean</span></span>

## <span data-ttu-id="abc43-141">Notas</span><span class="sxs-lookup"><span data-stu-id="abc43-141">NOTES</span></span>

## <span data-ttu-id="abc43-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abc43-142">RELATED LINKS</span></span>
