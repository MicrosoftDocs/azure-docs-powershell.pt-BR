---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 5aa70f15b5f542b36420e5f8df1cc65bb5dbd09a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892243"
---
# <span data-ttu-id="be814-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="be814-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="be814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be814-102">SYNOPSIS</span></span>
<span data-ttu-id="be814-103">Modifica a configuração do nó para a que um nó DSC é mapeado.</span><span class="sxs-lookup"><span data-stu-id="be814-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="be814-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="be814-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be814-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="be814-105">DESCRIPTION</span></span>
<span data-ttu-id="be814-106">O cmdlet **Set-AzAutomationDscNode** modifica uma configuração de nó DSC (Configuração de Estado Desejado) do APS.</span><span class="sxs-lookup"><span data-stu-id="be814-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="be814-107">A Automação do Azure armazena a configuração do nó DSC como um documento de configuração do Formato de Objeto Gerenciado (MOF).</span><span class="sxs-lookup"><span data-stu-id="be814-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="be814-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be814-108">EXAMPLES</span></span>

### <span data-ttu-id="be814-109">Exemplo 1: Modificar o mapeamento de configuração do nó</span><span class="sxs-lookup"><span data-stu-id="be814-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="be814-110">Este comando atribui a configuração do nó chamada Contoso.NodeConfiguration01 ao nó que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="be814-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="be814-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="be814-111">PARAMETERS</span></span>

### <span data-ttu-id="be814-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="be814-112">-AutomationAccountName</span></span>
<span data-ttu-id="be814-113">Especifica o nome da conta de Automação que contém o nó DSC para o qual esse cmdlet modifica a configuração.</span><span class="sxs-lookup"><span data-stu-id="be814-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be814-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be814-114">-DefaultProfile</span></span>
<span data-ttu-id="be814-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="be814-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be814-116">-Force</span><span class="sxs-lookup"><span data-stu-id="be814-116">-Force</span></span>
<span data-ttu-id="be814-117">ps_force o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="be814-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be814-118">-Id</span><span class="sxs-lookup"><span data-stu-id="be814-118">-Id</span></span>
<span data-ttu-id="be814-119">Especifica a ID exclusiva do nó DSC para o qual esse cmdlet modifica a configuração.</span><span class="sxs-lookup"><span data-stu-id="be814-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be814-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="be814-120">-NodeConfigurationName</span></span>
<span data-ttu-id="be814-121">Especifica o nome da configuração do nó à qual esse cmdlet mapeia o nó.</span><span class="sxs-lookup"><span data-stu-id="be814-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="be814-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be814-122">-ResourceGroupName</span></span>
<span data-ttu-id="be814-123">Especifica o nome de um grupo de recursos no qual esse cmdlet modifica uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="be814-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be814-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be814-124">-Confirm</span></span>
<span data-ttu-id="be814-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be814-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be814-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be814-126">-WhatIf</span></span>
<span data-ttu-id="be814-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be814-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be814-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be814-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be814-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be814-129">CommonParameters</span></span>
<span data-ttu-id="be814-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be814-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be814-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be814-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be814-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be814-132">INPUTS</span></span>

### <span data-ttu-id="be814-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="be814-133">System.Guid</span></span>

### <span data-ttu-id="be814-134">System.String</span><span class="sxs-lookup"><span data-stu-id="be814-134">System.String</span></span>

## <span data-ttu-id="be814-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="be814-135">OUTPUTS</span></span>

### <span data-ttu-id="be814-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="be814-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="be814-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="be814-137">NOTES</span></span>

## <span data-ttu-id="be814-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be814-138">RELATED LINKS</span></span>

[<span data-ttu-id="be814-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="be814-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="be814-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="be814-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="be814-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="be814-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


