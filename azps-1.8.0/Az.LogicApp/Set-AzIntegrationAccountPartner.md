---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: ae9b9f37a20f63a502da2904fd6d94f8a6aa281f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770466"
---
# <span data-ttu-id="f9230-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f9230-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="f9230-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9230-102">SYNOPSIS</span></span>
<span data-ttu-id="f9230-103">Modifica um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f9230-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="f9230-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9230-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9230-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9230-105">DESCRIPTION</span></span>
<span data-ttu-id="f9230-106">O cmdlet **set-AzIntegrationAccountPartner** modifica um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f9230-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="f9230-107">Esse cmdlet retorna um objeto que representa o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f9230-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="f9230-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do parceiro.</span><span class="sxs-lookup"><span data-stu-id="f9230-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="f9230-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="f9230-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f9230-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="f9230-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f9230-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f9230-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f9230-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="f9230-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f9230-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9230-113">EXAMPLES</span></span>

### <span data-ttu-id="f9230-114">Exemplo 1: modificar um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="f9230-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="f9230-115">Esse comando modifica o parceiro da conta de integração chamado IntegrationAccountPartner22 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f9230-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="f9230-116">OS</span><span class="sxs-lookup"><span data-stu-id="f9230-116">PARAMETERS</span></span>

### <span data-ttu-id="f9230-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="f9230-117">-BusinessIdentities</span></span>
<span data-ttu-id="f9230-118">Especifica as identidades comerciais para o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f9230-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="f9230-119">Especifique uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f9230-119">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9230-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9230-120">-DefaultProfile</span></span>
<span data-ttu-id="f9230-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f9230-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9230-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f9230-122">-Force</span></span>
<span data-ttu-id="f9230-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9230-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9230-124">-Metadados</span><span class="sxs-lookup"><span data-stu-id="f9230-124">-Metadata</span></span>
<span data-ttu-id="f9230-125">Especifica um objeto de metadados para o parceiro.</span><span class="sxs-lookup"><span data-stu-id="f9230-125">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9230-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9230-126">-Name</span></span>
<span data-ttu-id="f9230-127">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f9230-127">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9230-128">-Partnername</span><span class="sxs-lookup"><span data-stu-id="f9230-128">-PartnerName</span></span>
<span data-ttu-id="f9230-129">Especifica o nome do parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f9230-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="f9230-130">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="f9230-130">-PartnerType</span></span>
<span data-ttu-id="f9230-131">Especifica o tipo da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f9230-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="f9230-132">Esse parâmetro dá suporte para o tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="f9230-132">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9230-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9230-133">-ResourceGroupName</span></span>
<span data-ttu-id="f9230-134">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9230-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f9230-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9230-135">-Confirm</span></span>
<span data-ttu-id="f9230-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9230-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9230-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9230-137">-WhatIf</span></span>
<span data-ttu-id="f9230-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9230-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9230-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9230-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9230-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9230-140">CommonParameters</span></span>
<span data-ttu-id="f9230-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9230-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9230-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9230-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9230-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9230-143">INPUTS</span></span>

### <span data-ttu-id="f9230-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f9230-144">System.String</span></span>

## <span data-ttu-id="f9230-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9230-145">OUTPUTS</span></span>

### <span data-ttu-id="f9230-146">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f9230-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="f9230-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9230-147">NOTES</span></span>

## <span data-ttu-id="f9230-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9230-148">RELATED LINKS</span></span>

[<span data-ttu-id="f9230-149">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f9230-149">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f9230-150">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f9230-150">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f9230-151">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f9230-151">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


