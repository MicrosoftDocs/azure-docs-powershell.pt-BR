---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: 4c50f7de3d3748f254d87910fc8c55bb0ba8fc22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887117"
---
# <span data-ttu-id="1bf22-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1bf22-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="1bf22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf22-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf22-103">Remove um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1bf22-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="1bf22-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1bf22-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf22-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1bf22-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf22-106">O cmdlet **Remove-AzIntegrationAccountPartner** remove um parceiro de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1bf22-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="1bf22-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do parceiro.</span><span class="sxs-lookup"><span data-stu-id="1bf22-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="1bf22-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="1bf22-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1bf22-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="1bf22-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1bf22-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1bf22-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1bf22-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="1bf22-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1bf22-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bf22-112">EXAMPLES</span></span>

### <span data-ttu-id="1bf22-113">Exemplo 1: Remover um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="1bf22-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="1bf22-114">Este comando remove o parceiro de conta de integração chamado IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="1bf22-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="1bf22-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1bf22-115">PARAMETERS</span></span>

### <span data-ttu-id="1bf22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf22-116">-DefaultProfile</span></span>
<span data-ttu-id="1bf22-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1bf22-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bf22-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1bf22-118">-Force</span></span>
<span data-ttu-id="1bf22-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1bf22-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1bf22-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1bf22-120">-Name</span></span>
<span data-ttu-id="1bf22-121">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1bf22-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf22-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="1bf22-122">-PartnerName</span></span>
<span data-ttu-id="1bf22-123">Especifica o nome do parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1bf22-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf22-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf22-124">-ResourceGroupName</span></span>
<span data-ttu-id="1bf22-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1bf22-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1bf22-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bf22-126">-Confirm</span></span>
<span data-ttu-id="1bf22-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bf22-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf22-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf22-128">-WhatIf</span></span>
<span data-ttu-id="1bf22-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1bf22-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bf22-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1bf22-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf22-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf22-131">CommonParameters</span></span>
<span data-ttu-id="1bf22-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf22-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf22-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf22-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf22-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bf22-134">INPUTS</span></span>

### <span data-ttu-id="1bf22-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1bf22-135">System.String</span></span>

## <span data-ttu-id="1bf22-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1bf22-136">OUTPUTS</span></span>

### <span data-ttu-id="1bf22-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="1bf22-137">System.Void</span></span>

## <span data-ttu-id="1bf22-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="1bf22-138">NOTES</span></span>

## <span data-ttu-id="1bf22-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bf22-139">RELATED LINKS</span></span>

[<span data-ttu-id="1bf22-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1bf22-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="1bf22-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1bf22-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="1bf22-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1bf22-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


