---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 02a6d7a129dc084b982f1827d678354265ddbc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112252"
---
# <span data-ttu-id="94c40-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="94c40-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="94c40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94c40-102">SYNOPSIS</span></span>
<span data-ttu-id="94c40-103">Modifica a configuração do nó para a onde um nó DSC está mapeado.</span><span class="sxs-lookup"><span data-stu-id="94c40-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="94c40-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94c40-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94c40-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="94c40-105">DESCRIPTION</span></span>
<span data-ttu-id="94c40-106">O cmdlet **Set-AzAutomationDscNode** modifica uma configuração de nó DSC (Configuração de Estado Desejado) APS.</span><span class="sxs-lookup"><span data-stu-id="94c40-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="94c40-107">A Automação do Azure armazena a configuração do nó DSC como um documento de configuração MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="94c40-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="94c40-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="94c40-108">EXAMPLES</span></span>

### <span data-ttu-id="94c40-109">Exemplo 1: Modificar o mapeamento de configuração do nó</span><span class="sxs-lookup"><span data-stu-id="94c40-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="94c40-110">Esse comando atribui a configuração do nó chamada Contoso.NodeConfiguration01 ao nó que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="94c40-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="94c40-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94c40-111">PARAMETERS</span></span>

### <span data-ttu-id="94c40-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94c40-112">-AutomationAccountName</span></span>
<span data-ttu-id="94c40-113">Especifica o nome da conta automação que contém o nó DSC para o qual esse cmdlet modifica a configuração.</span><span class="sxs-lookup"><span data-stu-id="94c40-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="94c40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c40-114">-DefaultProfile</span></span>
<span data-ttu-id="94c40-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="94c40-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94c40-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="94c40-116">-Force</span></span>
<span data-ttu-id="94c40-117">ps_force comando a ser executado sem precisar de confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="94c40-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94c40-118">-ID</span><span class="sxs-lookup"><span data-stu-id="94c40-118">-Id</span></span>
<span data-ttu-id="94c40-119">Especifica a ID exclusiva do nó DSC para o qual esse cmdlet modifica a configuração.</span><span class="sxs-lookup"><span data-stu-id="94c40-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="94c40-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="94c40-120">-NodeConfigurationName</span></span>
<span data-ttu-id="94c40-121">Especifica o nome da configuração do nó à qual esse cmdlet mapeia o nó.</span><span class="sxs-lookup"><span data-stu-id="94c40-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="94c40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c40-122">-ResourceGroupName</span></span>
<span data-ttu-id="94c40-123">Especifica o nome de um grupo de recursos no qual esse cmdlet modifica uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="94c40-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="94c40-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="94c40-124">-Confirm</span></span>
<span data-ttu-id="94c40-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c40-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c40-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c40-126">-WhatIf</span></span>
<span data-ttu-id="94c40-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="94c40-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c40-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94c40-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c40-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c40-129">CommonParameters</span></span>
<span data-ttu-id="94c40-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c40-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c40-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c40-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c40-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="94c40-132">INPUTS</span></span>

### <span data-ttu-id="94c40-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="94c40-133">System.Guid</span></span>

### <span data-ttu-id="94c40-134">System.String</span><span class="sxs-lookup"><span data-stu-id="94c40-134">System.String</span></span>

## <span data-ttu-id="94c40-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="94c40-135">OUTPUTS</span></span>

### <span data-ttu-id="94c40-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="94c40-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="94c40-137">Notas</span><span class="sxs-lookup"><span data-stu-id="94c40-137">NOTES</span></span>

## <span data-ttu-id="94c40-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94c40-138">RELATED LINKS</span></span>

[<span data-ttu-id="94c40-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="94c40-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="94c40-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="94c40-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="94c40-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="94c40-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


