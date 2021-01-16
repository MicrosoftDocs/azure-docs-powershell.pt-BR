---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260372"
---
# <span data-ttu-id="64198-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="64198-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="64198-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64198-102">SYNOPSIS</span></span>
<span data-ttu-id="64198-103">Remove um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="64198-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="64198-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64198-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64198-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64198-105">DESCRIPTION</span></span>
<span data-ttu-id="64198-106">O cmdlet **Remove-AzIntegrationAccountPartner** remove um parceiro de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64198-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="64198-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do parceiro.</span><span class="sxs-lookup"><span data-stu-id="64198-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="64198-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="64198-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="64198-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="64198-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="64198-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="64198-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="64198-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="64198-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="64198-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64198-112">EXAMPLES</span></span>

### <span data-ttu-id="64198-113">Exemplo 1: remover um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="64198-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="64198-114">Esse comando Remove o parceiro da conta de integração chamado IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="64198-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="64198-115">OS</span><span class="sxs-lookup"><span data-stu-id="64198-115">PARAMETERS</span></span>

### <span data-ttu-id="64198-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64198-116">-DefaultProfile</span></span>
<span data-ttu-id="64198-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="64198-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64198-118">-Force</span><span class="sxs-lookup"><span data-stu-id="64198-118">-Force</span></span>
<span data-ttu-id="64198-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="64198-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64198-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="64198-120">-Name</span></span>
<span data-ttu-id="64198-121">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="64198-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="64198-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="64198-122">-PartnerName</span></span>
<span data-ttu-id="64198-123">Especifica o nome do parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="64198-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="64198-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64198-124">-ResourceGroupName</span></span>
<span data-ttu-id="64198-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64198-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="64198-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64198-126">-Confirm</span></span>
<span data-ttu-id="64198-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64198-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64198-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64198-128">-WhatIf</span></span>
<span data-ttu-id="64198-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64198-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64198-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64198-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64198-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64198-131">CommonParameters</span></span>
<span data-ttu-id="64198-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64198-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64198-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64198-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64198-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64198-134">INPUTS</span></span>

### <span data-ttu-id="64198-135">System. String</span><span class="sxs-lookup"><span data-stu-id="64198-135">System.String</span></span>

## <span data-ttu-id="64198-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64198-136">OUTPUTS</span></span>

### <span data-ttu-id="64198-137">System. void</span><span class="sxs-lookup"><span data-stu-id="64198-137">System.Void</span></span>

## <span data-ttu-id="64198-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64198-138">NOTES</span></span>

## <span data-ttu-id="64198-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64198-139">RELATED LINKS</span></span>

[<span data-ttu-id="64198-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="64198-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="64198-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="64198-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="64198-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="64198-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


