---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 82fb412cca4642881ff6a84ede1f2c722c6d5086
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892757"
---
# <span data-ttu-id="d4317-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4317-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="d4317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4317-102">SYNOPSIS</span></span>
<span data-ttu-id="d4317-103">Cria um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="d4317-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d4317-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4317-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d4317-105">DESCRIPTION</span></span>
<span data-ttu-id="d4317-106">O cmdlet **New-AzIntegrationAccountAgreement** cria um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="d4317-107">Este cmdlet retorna um objeto que representa o contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="d4317-108">Especifique o nome da conta de integração, o nome do grupo de recursos, o nome do contrato, o tipo, o nome do parceiro, os qualificadores do parceiro e o conteúdo do contrato.</span><span class="sxs-lookup"><span data-stu-id="d4317-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="d4317-109">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores de parâmetro de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="d4317-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="d4317-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="d4317-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d4317-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="d4317-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d4317-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d4317-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d4317-113">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="d4317-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d4317-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4317-114">EXAMPLES</span></span>

### <span data-ttu-id="d4317-115">Exemplo 1: Criar um contrato de conta de integração</span><span class="sxs-lookup"><span data-stu-id="d4317-115">Example 1: Create a integration account agreement</span></span>
```powershell
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="d4317-116">Este comando cria um contrato de conta de integração no grupo de recursos do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="d4317-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="d4317-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d4317-117">Example 2</span></span>

<span data-ttu-id="d4317-118">Cria um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-118">Creates an integration account agreement.</span></span> <span data-ttu-id="d4317-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d4317-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="d4317-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d4317-120">PARAMETERS</span></span>

### <span data-ttu-id="d4317-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="d4317-121">-AgreementContent</span></span>
<span data-ttu-id="d4317-122">Especifica o conteúdo do contrato, no formato JSON (Notação de Objeto JavaScript), para o contrato.</span><span class="sxs-lookup"><span data-stu-id="d4317-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="d4317-123">Especifique esse parâmetro ou *o parâmetro AgreementContentFilePath.*</span><span class="sxs-lookup"><span data-stu-id="d4317-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4317-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="d4317-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="d4317-125">Especifica o caminho do arquivo do conteúdo do contrato para o contrato.</span><span class="sxs-lookup"><span data-stu-id="d4317-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="d4317-126">Especifique esse parâmetro ou o *parâmetro AgreementContent.*</span><span class="sxs-lookup"><span data-stu-id="d4317-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4317-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d4317-127">-AgreementName</span></span>
<span data-ttu-id="d4317-128">Especifica um nome para o contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="d4317-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d4317-129">-AgreementType</span></span>
<span data-ttu-id="d4317-130">Especifica o tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="d4317-131">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d4317-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d4317-132">X12</span><span class="sxs-lookup"><span data-stu-id="d4317-132">X12</span></span> 
- <span data-ttu-id="d4317-133">AS2</span><span class="sxs-lookup"><span data-stu-id="d4317-133">AS2</span></span>
- <span data-ttu-id="d4317-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="d4317-134">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4317-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4317-135">-DefaultProfile</span></span>
<span data-ttu-id="d4317-136">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d4317-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4317-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="d4317-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="d4317-138">Especifica um qualificador de identidade comercial de nome para o parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="d4317-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="d4317-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="d4317-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="d4317-140">O valor do qualificador de identidade de convidado do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="d4317-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="d4317-141">-GuestPartner</span></span>
<span data-ttu-id="d4317-142">Especifica o nome do parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="d4317-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="d4317-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="d4317-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="d4317-144">Especifica um qualificador de identidade comercial de nome para o parceiro host.</span><span class="sxs-lookup"><span data-stu-id="d4317-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="d4317-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="d4317-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="d4317-146">O valor do qualificador de identidade do host do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="d4317-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="d4317-147">-HostPartner</span></span>
<span data-ttu-id="d4317-148">Especifica o nome do parceiro host.</span><span class="sxs-lookup"><span data-stu-id="d4317-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="d4317-149">-Metadados</span><span class="sxs-lookup"><span data-stu-id="d4317-149">-Metadata</span></span>
<span data-ttu-id="d4317-150">Especifica um objeto de metadados para o contrato.</span><span class="sxs-lookup"><span data-stu-id="d4317-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="d4317-151">-Name</span><span class="sxs-lookup"><span data-stu-id="d4317-151">-Name</span></span>
<span data-ttu-id="d4317-152">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d4317-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="d4317-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4317-153">-ResourceGroupName</span></span>
<span data-ttu-id="d4317-154">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4317-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d4317-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4317-155">-Confirm</span></span>
<span data-ttu-id="d4317-156">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4317-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4317-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4317-157">-WhatIf</span></span>
<span data-ttu-id="d4317-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4317-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4317-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4317-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4317-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4317-160">CommonParameters</span></span>
<span data-ttu-id="d4317-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4317-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4317-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4317-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4317-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4317-163">INPUTS</span></span>

### <span data-ttu-id="d4317-164">System.String</span><span class="sxs-lookup"><span data-stu-id="d4317-164">System.String</span></span>

## <span data-ttu-id="d4317-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d4317-165">OUTPUTS</span></span>

### <span data-ttu-id="d4317-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4317-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="d4317-167">NOTES</span><span class="sxs-lookup"><span data-stu-id="d4317-167">NOTES</span></span>

## <span data-ttu-id="d4317-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4317-168">RELATED LINKS</span></span>

[<span data-ttu-id="d4317-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4317-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="d4317-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4317-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="d4317-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4317-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


