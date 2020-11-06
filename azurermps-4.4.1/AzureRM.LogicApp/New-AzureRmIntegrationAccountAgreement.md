---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: b95ab13e7ea35e1b41f449f461892e7ea324aa97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611108"
---
# <span data-ttu-id="75d3f-101">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="75d3f-101">New-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="75d3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="75d3f-103">Cria um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="75d3f-103">Creates an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75d3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75d3f-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75d3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="75d3f-106">O cmdlet **New-AzureRmIntegrationAccountAgreement** cria um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="75d3f-106">The **New-AzureRmIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="75d3f-107">Esse cmdlet retorna um objeto que representa o contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="75d3f-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="75d3f-108">Especifique o nome da conta de integração, o nome do grupo de recursos, o nome do contrato, o tipo, o nome do parceiro, os qualificadores parceiros e o conteúdo do contrato.</span><span class="sxs-lookup"><span data-stu-id="75d3f-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>

<span data-ttu-id="75d3f-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="75d3f-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="75d3f-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="75d3f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="75d3f-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="75d3f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="75d3f-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="75d3f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="75d3f-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="75d3f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="75d3f-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75d3f-114">EXAMPLES</span></span>

### <span data-ttu-id="75d3f-115">Exemplo 1: criar um contrato de conta de integração</span><span class="sxs-lookup"><span data-stu-id="75d3f-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="75d3f-116">Esse comando cria um contrato de conta de integração no grupo de recursos do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="75d3f-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="75d3f-117">OS</span><span class="sxs-lookup"><span data-stu-id="75d3f-117">PARAMETERS</span></span>

### <span data-ttu-id="75d3f-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="75d3f-118">-AgreementContent</span></span>
<span data-ttu-id="75d3f-119">Especifica o conteúdo do contrato, no formato JSON (JavaScript Object Notation), para o contrato.</span><span class="sxs-lookup"><span data-stu-id="75d3f-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="75d3f-120">Especifique esse parâmetro ou o parâmetro *AgreementContentFilePath* .</span><span class="sxs-lookup"><span data-stu-id="75d3f-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="75d3f-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="75d3f-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="75d3f-122">Especifica o caminho de arquivo do conteúdo do contrato para o contrato.</span><span class="sxs-lookup"><span data-stu-id="75d3f-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="75d3f-123">Especifique esse parâmetro ou o parâmetro *AgreementContent* .</span><span class="sxs-lookup"><span data-stu-id="75d3f-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="75d3f-124">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="75d3f-124">-AgreementName</span></span>
<span data-ttu-id="75d3f-125">Especifica um nome para o contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="75d3f-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="75d3f-126">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="75d3f-126">-AgreementType</span></span>
<span data-ttu-id="75d3f-127">Especifica o tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="75d3f-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="75d3f-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="75d3f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75d3f-129">X12</span><span class="sxs-lookup"><span data-stu-id="75d3f-129">X12</span></span> 
- <span data-ttu-id="75d3f-130">AS2</span><span class="sxs-lookup"><span data-stu-id="75d3f-130">AS2</span></span>
- <span data-ttu-id="75d3f-131">Edifact</span><span class="sxs-lookup"><span data-stu-id="75d3f-131">Edifact</span></span>

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

### <span data-ttu-id="75d3f-132">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="75d3f-132">-GuestIdentityQualifier</span></span>
<span data-ttu-id="75d3f-133">Especifica um nome qualificador de identidade de empresa para o parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="75d3f-133">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="75d3f-134">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="75d3f-134">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="75d3f-135">O contrato da conta de integração é um valor qualificador de identidade de convidado.</span><span class="sxs-lookup"><span data-stu-id="75d3f-135">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="75d3f-136">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="75d3f-136">-GuestPartner</span></span>
<span data-ttu-id="75d3f-137">Especifica o nome do parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="75d3f-137">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="75d3f-138">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="75d3f-138">-HostIdentityQualifier</span></span>
<span data-ttu-id="75d3f-139">Especifica um nome qualificador de identidade de empresa para o parceiro do host.</span><span class="sxs-lookup"><span data-stu-id="75d3f-139">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="75d3f-140">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="75d3f-140">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="75d3f-141">O valor do qualificador de identidade de host do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="75d3f-141">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="75d3f-142">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="75d3f-142">-HostPartner</span></span>
<span data-ttu-id="75d3f-143">Especifica o nome do parceiro do host.</span><span class="sxs-lookup"><span data-stu-id="75d3f-143">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="75d3f-144">-Metadados</span><span class="sxs-lookup"><span data-stu-id="75d3f-144">-Metadata</span></span>
<span data-ttu-id="75d3f-145">Especifica um objeto de metadados para o contrato.</span><span class="sxs-lookup"><span data-stu-id="75d3f-145">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="75d3f-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="75d3f-146">-Name</span></span>
<span data-ttu-id="75d3f-147">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="75d3f-147">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="75d3f-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d3f-148">-ResourceGroupName</span></span>
<span data-ttu-id="75d3f-149">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75d3f-149">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="75d3f-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75d3f-150">-Confirm</span></span>
<span data-ttu-id="75d3f-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75d3f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d3f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d3f-152">-WhatIf</span></span>
<span data-ttu-id="75d3f-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75d3f-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75d3f-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75d3f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75d3f-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d3f-155">-DefaultProfile</span></span>
<span data-ttu-id="75d3f-156">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75d3f-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d3f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d3f-157">CommonParameters</span></span>
<span data-ttu-id="75d3f-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d3f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d3f-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d3f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d3f-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75d3f-160">INPUTS</span></span>

## <span data-ttu-id="75d3f-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75d3f-161">OUTPUTS</span></span>

### <span data-ttu-id="75d3f-162">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="75d3f-162">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="75d3f-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75d3f-163">NOTES</span></span>

## <span data-ttu-id="75d3f-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75d3f-164">RELATED LINKS</span></span>

[<span data-ttu-id="75d3f-165">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="75d3f-165">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="75d3f-166">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="75d3f-166">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="75d3f-167">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="75d3f-167">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


