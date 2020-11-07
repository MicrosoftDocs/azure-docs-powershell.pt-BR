---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: bbd64f1e6df016efe0bdd22bb0ae848c79566edf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777349"
---
# <span data-ttu-id="81b70-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="81b70-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="81b70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81b70-102">SYNOPSIS</span></span>
<span data-ttu-id="81b70-103">Cria um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="81b70-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="81b70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81b70-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81b70-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81b70-105">DESCRIPTION</span></span>
<span data-ttu-id="81b70-106">O cmdlet **New-AzIntegrationAccountPartner** cria um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="81b70-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="81b70-107">Esse cmdlet retorna um objeto que representa o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="81b70-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="81b70-108">Especifique o nome da conta de integração, o nome do grupo de recursos, o nome do parceiro e as identidades dos parceiros.</span><span class="sxs-lookup"><span data-stu-id="81b70-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="81b70-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="81b70-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="81b70-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="81b70-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="81b70-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="81b70-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="81b70-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="81b70-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="81b70-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="81b70-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="81b70-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81b70-114">EXAMPLES</span></span>

### <span data-ttu-id="81b70-115">Exemplo 1: criar um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="81b70-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="81b70-116">Esse comando cria o parceiro de conta de integração chamado IntegrationAccountPartner22 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="81b70-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="81b70-117">OS</span><span class="sxs-lookup"><span data-stu-id="81b70-117">PARAMETERS</span></span>

### <span data-ttu-id="81b70-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="81b70-118">-BusinessIdentities</span></span>
<span data-ttu-id="81b70-119">Especifica as identidades comerciais para o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="81b70-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="81b70-120">Especifique uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="81b70-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b70-121">-DefaultProfile</span></span>
<span data-ttu-id="81b70-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="81b70-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81b70-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="81b70-123">-Metadata</span></span>
<span data-ttu-id="81b70-124">Especifica um objeto de metadados para o parceiro.</span><span class="sxs-lookup"><span data-stu-id="81b70-124">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="81b70-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="81b70-125">-Name</span></span>
<span data-ttu-id="81b70-126">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="81b70-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="81b70-127">-Partnername</span><span class="sxs-lookup"><span data-stu-id="81b70-127">-PartnerName</span></span>
<span data-ttu-id="81b70-128">Especifica um nome para o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="81b70-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="81b70-129">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="81b70-129">-PartnerType</span></span>
<span data-ttu-id="81b70-130">Especifica o tipo da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="81b70-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="81b70-131">Esse parâmetro dá suporte para o tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="81b70-131">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="81b70-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b70-132">-ResourceGroupName</span></span>
<span data-ttu-id="81b70-133">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81b70-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="81b70-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81b70-134">-Confirm</span></span>
<span data-ttu-id="81b70-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b70-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b70-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b70-136">-WhatIf</span></span>
<span data-ttu-id="81b70-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81b70-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b70-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81b70-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b70-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b70-139">CommonParameters</span></span>
<span data-ttu-id="81b70-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b70-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b70-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b70-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b70-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81b70-142">INPUTS</span></span>

### <span data-ttu-id="81b70-143">System. String</span><span class="sxs-lookup"><span data-stu-id="81b70-143">System.String</span></span>

## <span data-ttu-id="81b70-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81b70-144">OUTPUTS</span></span>

### <span data-ttu-id="81b70-145">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="81b70-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="81b70-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81b70-146">NOTES</span></span>

## <span data-ttu-id="81b70-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81b70-147">RELATED LINKS</span></span>

[<span data-ttu-id="81b70-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="81b70-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="81b70-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="81b70-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="81b70-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="81b70-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


