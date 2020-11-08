---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: edd50a72ed0614cf7c71dfbde9f487e8fe632d85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126063"
---
# <span data-ttu-id="7ead5-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ead5-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="7ead5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ead5-102">SYNOPSIS</span></span>
<span data-ttu-id="7ead5-103">Modifica um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7ead5-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="7ead5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ead5-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ead5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ead5-105">DESCRIPTION</span></span>
<span data-ttu-id="7ead5-106">O cmdlet **set-AzIntegrationAccountPartner** modifica um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7ead5-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="7ead5-107">Esse cmdlet retorna um objeto que representa o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7ead5-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="7ead5-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do parceiro.</span><span class="sxs-lookup"><span data-stu-id="7ead5-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="7ead5-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="7ead5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7ead5-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="7ead5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7ead5-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7ead5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7ead5-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="7ead5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7ead5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ead5-113">EXAMPLES</span></span>

### <span data-ttu-id="7ead5-114">Exemplo 1: modificar um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="7ead5-114">Example 1: Modify an integration account partner</span></span>
```powershell
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

<span data-ttu-id="7ead5-115">Esse comando modifica o parceiro da conta de integração chamado IntegrationAccountPartner22 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="7ead5-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

### <span data-ttu-id="7ead5-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7ead5-116">Example 2</span></span>

<span data-ttu-id="7ead5-117">Modifica um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7ead5-117">Modifies an integration account partner.</span></span> <span data-ttu-id="7ead5-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="7ead5-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountPartner -BusinessIdentities <Object> -Metadata <Object> -Name 'IntegrationAccount31' -PartnerName 'IntegrationAccountPartner22' -PartnerType B2B -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="7ead5-119">OS</span><span class="sxs-lookup"><span data-stu-id="7ead5-119">PARAMETERS</span></span>

### <span data-ttu-id="7ead5-120">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="7ead5-120">-BusinessIdentities</span></span>
<span data-ttu-id="7ead5-121">Especifica as identidades comerciais para o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7ead5-121">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="7ead5-122">Especifique uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7ead5-122">Specify a hash table.</span></span>

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

### <span data-ttu-id="7ead5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ead5-123">-DefaultProfile</span></span>
<span data-ttu-id="7ead5-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7ead5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ead5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7ead5-125">-Force</span></span>
<span data-ttu-id="7ead5-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7ead5-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ead5-127">-Metadados</span><span class="sxs-lookup"><span data-stu-id="7ead5-127">-Metadata</span></span>
<span data-ttu-id="7ead5-128">Especifica um objeto de metadados para o parceiro.</span><span class="sxs-lookup"><span data-stu-id="7ead5-128">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="7ead5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ead5-129">-Name</span></span>
<span data-ttu-id="7ead5-130">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7ead5-130">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="7ead5-131">-Partnername</span><span class="sxs-lookup"><span data-stu-id="7ead5-131">-PartnerName</span></span>
<span data-ttu-id="7ead5-132">Especifica o nome do parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7ead5-132">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="7ead5-133">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="7ead5-133">-PartnerType</span></span>
<span data-ttu-id="7ead5-134">Especifica o tipo da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7ead5-134">Specifies the type of the integration account.</span></span>
<span data-ttu-id="7ead5-135">Esse parâmetro dá suporte para o tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="7ead5-135">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="7ead5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ead5-136">-ResourceGroupName</span></span>
<span data-ttu-id="7ead5-137">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ead5-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7ead5-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ead5-138">-Confirm</span></span>
<span data-ttu-id="7ead5-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ead5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ead5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ead5-140">-WhatIf</span></span>
<span data-ttu-id="7ead5-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ead5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ead5-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ead5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ead5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ead5-143">CommonParameters</span></span>
<span data-ttu-id="7ead5-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ead5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ead5-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ead5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ead5-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ead5-146">INPUTS</span></span>

### <span data-ttu-id="7ead5-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7ead5-147">System.String</span></span>

## <span data-ttu-id="7ead5-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ead5-148">OUTPUTS</span></span>

### <span data-ttu-id="7ead5-149">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ead5-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="7ead5-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ead5-150">NOTES</span></span>

## <span data-ttu-id="7ead5-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ead5-151">RELATED LINKS</span></span>

[<span data-ttu-id="7ead5-152">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ead5-152">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="7ead5-153">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ead5-153">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="7ead5-154">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ead5-154">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


