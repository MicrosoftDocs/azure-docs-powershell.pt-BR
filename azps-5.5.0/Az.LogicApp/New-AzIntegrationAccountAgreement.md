---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113016"
---
# <span data-ttu-id="d902e-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d902e-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="d902e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d902e-102">SYNOPSIS</span></span>
<span data-ttu-id="d902e-103">Cria um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d902e-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="d902e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d902e-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d902e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d902e-105">DESCRIPTION</span></span>
<span data-ttu-id="d902e-106">O **cmdlet New-AzIntegrationAccountAgreement** cria um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d902e-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="d902e-107">Este cmdlet retorna um objeto que representa o contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d902e-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="d902e-108">Especifique o nome da conta de integração, o nome do grupo de recursos, o nome do contrato, o tipo, o nome do parceiro, os qualificadores do parceiro e o conteúdo do contrato.</span><span class="sxs-lookup"><span data-stu-id="d902e-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="d902e-109">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores de parâmetros de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="d902e-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="d902e-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="d902e-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d902e-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="d902e-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d902e-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d902e-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d902e-113">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="d902e-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d902e-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d902e-114">EXAMPLES</span></span>

### <span data-ttu-id="d902e-115">Exemplo 1: Criar um contrato de conta de integração</span><span class="sxs-lookup"><span data-stu-id="d902e-115">Example 1: Create a integration account agreement</span></span>
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

<span data-ttu-id="d902e-116">Esse comando cria um contrato de conta de integração no grupo de recursos do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="d902e-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="d902e-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d902e-117">Example 2</span></span>

<span data-ttu-id="d902e-118">Cria um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d902e-118">Creates an integration account agreement.</span></span> <span data-ttu-id="d902e-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d902e-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="d902e-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d902e-120">PARAMETERS</span></span>

### <span data-ttu-id="d902e-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="d902e-121">-AgreementContent</span></span>
<span data-ttu-id="d902e-122">Especifica o conteúdo do contrato, no formato JSON (Notação de Objeto JavaScript), para o contrato.</span><span class="sxs-lookup"><span data-stu-id="d902e-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="d902e-123">Especifique esse parâmetro ou o parâmetro *AgreementContentFilePath.*</span><span class="sxs-lookup"><span data-stu-id="d902e-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="d902e-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="d902e-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="d902e-125">Especifica o caminho do arquivo do conteúdo do contrato.</span><span class="sxs-lookup"><span data-stu-id="d902e-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="d902e-126">Especifique esse parâmetro ou o parâmetro *AgreementContent.*</span><span class="sxs-lookup"><span data-stu-id="d902e-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="d902e-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d902e-127">-AgreementName</span></span>
<span data-ttu-id="d902e-128">Especifica um nome para o contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d902e-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="d902e-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d902e-129">-AgreementType</span></span>
<span data-ttu-id="d902e-130">Especifica o tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d902e-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="d902e-131">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d902e-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d902e-132">X12</span><span class="sxs-lookup"><span data-stu-id="d902e-132">X12</span></span> 
- <span data-ttu-id="d902e-133">AS2</span><span class="sxs-lookup"><span data-stu-id="d902e-133">AS2</span></span>
- <span data-ttu-id="d902e-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="d902e-134">Edifact</span></span>

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

### <span data-ttu-id="d902e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d902e-135">-DefaultProfile</span></span>
<span data-ttu-id="d902e-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d902e-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d902e-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="d902e-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="d902e-138">Especifica um qualificador de identidade de negócios de nome para o parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="d902e-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="d902e-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="d902e-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="d902e-140">O valor qualificador do contrato de identidade de convidado do contrato de integração.</span><span class="sxs-lookup"><span data-stu-id="d902e-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="d902e-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="d902e-141">-GuestPartner</span></span>
<span data-ttu-id="d902e-142">Especifica o nome do parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="d902e-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="d902e-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="d902e-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="d902e-144">Especifica um qualificador de identidade de negócios de nome para o parceiro host.</span><span class="sxs-lookup"><span data-stu-id="d902e-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="d902e-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="d902e-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="d902e-146">O valor qualificador de identidade de host do contrato de integração de conta.</span><span class="sxs-lookup"><span data-stu-id="d902e-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="d902e-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="d902e-147">-HostPartner</span></span>
<span data-ttu-id="d902e-148">Especifica o nome do parceiro host.</span><span class="sxs-lookup"><span data-stu-id="d902e-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="d902e-149">-Metadados</span><span class="sxs-lookup"><span data-stu-id="d902e-149">-Metadata</span></span>
<span data-ttu-id="d902e-150">Especifica um objeto de metadados para o contrato.</span><span class="sxs-lookup"><span data-stu-id="d902e-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="d902e-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="d902e-151">-Name</span></span>
<span data-ttu-id="d902e-152">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d902e-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="d902e-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d902e-153">-ResourceGroupName</span></span>
<span data-ttu-id="d902e-154">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d902e-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d902e-155">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d902e-155">-Confirm</span></span>
<span data-ttu-id="d902e-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d902e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d902e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d902e-157">-WhatIf</span></span>
<span data-ttu-id="d902e-158">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d902e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d902e-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d902e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d902e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d902e-160">CommonParameters</span></span>
<span data-ttu-id="d902e-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d902e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d902e-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d902e-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d902e-163">Entradas</span><span class="sxs-lookup"><span data-stu-id="d902e-163">INPUTS</span></span>

### <span data-ttu-id="d902e-164">System.String</span><span class="sxs-lookup"><span data-stu-id="d902e-164">System.String</span></span>

## <span data-ttu-id="d902e-165">Saídas</span><span class="sxs-lookup"><span data-stu-id="d902e-165">OUTPUTS</span></span>

### <span data-ttu-id="d902e-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d902e-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="d902e-167">Notas</span><span class="sxs-lookup"><span data-stu-id="d902e-167">NOTES</span></span>

## <span data-ttu-id="d902e-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d902e-168">RELATED LINKS</span></span>

[<span data-ttu-id="d902e-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d902e-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="d902e-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d902e-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="d902e-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d902e-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


