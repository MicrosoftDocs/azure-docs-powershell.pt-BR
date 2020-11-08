---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: ac0e5e89706e648d714e3f09ebad5dee7d7b4416
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114468"
---
# <span data-ttu-id="24677-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="24677-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="24677-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24677-102">SYNOPSIS</span></span>
<span data-ttu-id="24677-103">Modifica um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="24677-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="24677-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24677-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24677-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24677-105">DESCRIPTION</span></span>
<span data-ttu-id="24677-106">O cmdlet **set-AzIntegrationAccountAgreement** modifica um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="24677-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="24677-107">Esse cmdlet retorna um objeto que representa o contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="24677-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="24677-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="24677-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="24677-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="24677-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="24677-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="24677-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="24677-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="24677-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="24677-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="24677-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="24677-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="24677-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="24677-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24677-114">EXAMPLES</span></span>

### <span data-ttu-id="24677-115">Exemplo 1: atualizar um contrato de conta de integração</span><span class="sxs-lookup"><span data-stu-id="24677-115">Example 1: Update an integration account agreement</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="24677-116">Este comando atualiza um contrato de conta de integração no grupo de recursos do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="24677-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="24677-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="24677-117">Example 2</span></span>

<span data-ttu-id="24677-118">Modifica um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="24677-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="24677-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="24677-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="24677-120">OS</span><span class="sxs-lookup"><span data-stu-id="24677-120">PARAMETERS</span></span>

### <span data-ttu-id="24677-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="24677-121">-AgreementContent</span></span>
<span data-ttu-id="24677-122">Especifica o conteúdo do contrato, no formato JSON (JavaScript Object Notation), para o contrato.</span><span class="sxs-lookup"><span data-stu-id="24677-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="24677-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="24677-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="24677-124">Especifica o caminho de arquivo do conteúdo do contrato para o contrato.</span><span class="sxs-lookup"><span data-stu-id="24677-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="24677-125">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="24677-125">-AgreementName</span></span>
<span data-ttu-id="24677-126">Especifica o nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="24677-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="24677-127">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="24677-127">-AgreementType</span></span>
<span data-ttu-id="24677-128">Especifica o tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="24677-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="24677-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="24677-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="24677-130">X12</span><span class="sxs-lookup"><span data-stu-id="24677-130">X12</span></span> 
- <span data-ttu-id="24677-131">AS2</span><span class="sxs-lookup"><span data-stu-id="24677-131">AS2</span></span>
- <span data-ttu-id="24677-132">Edifact</span><span class="sxs-lookup"><span data-stu-id="24677-132">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24677-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24677-133">-DefaultProfile</span></span>
<span data-ttu-id="24677-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="24677-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24677-135">-Force</span><span class="sxs-lookup"><span data-stu-id="24677-135">-Force</span></span>
<span data-ttu-id="24677-136">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="24677-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24677-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="24677-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="24677-138">Especifica um nome qualificador de identidade de empresa para o parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="24677-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="24677-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="24677-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="24677-140">O contrato da conta de integração é um valor qualificador de identidade de convidado.</span><span class="sxs-lookup"><span data-stu-id="24677-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="24677-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="24677-141">-GuestPartner</span></span>
<span data-ttu-id="24677-142">Especifica o nome do parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="24677-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="24677-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="24677-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="24677-144">Especifica um nome qualificador de identidade de empresa para o parceiro do host.</span><span class="sxs-lookup"><span data-stu-id="24677-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="24677-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="24677-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="24677-146">O valor do qualificador de identidade de host do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="24677-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="24677-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="24677-147">-HostPartner</span></span>
<span data-ttu-id="24677-148">Especifica o nome do parceiro do host.</span><span class="sxs-lookup"><span data-stu-id="24677-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="24677-149">-Metadados</span><span class="sxs-lookup"><span data-stu-id="24677-149">-Metadata</span></span>
<span data-ttu-id="24677-150">Especifica um objeto de metadados para o contrato.</span><span class="sxs-lookup"><span data-stu-id="24677-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="24677-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="24677-151">-Name</span></span>
<span data-ttu-id="24677-152">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="24677-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="24677-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24677-153">-ResourceGroupName</span></span>
<span data-ttu-id="24677-154">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24677-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="24677-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24677-155">-Confirm</span></span>
<span data-ttu-id="24677-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24677-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24677-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24677-157">-WhatIf</span></span>
<span data-ttu-id="24677-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24677-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24677-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24677-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24677-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24677-160">CommonParameters</span></span>
<span data-ttu-id="24677-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24677-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24677-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24677-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24677-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24677-163">INPUTS</span></span>

### <span data-ttu-id="24677-164">System. String</span><span class="sxs-lookup"><span data-stu-id="24677-164">System.String</span></span>

## <span data-ttu-id="24677-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24677-165">OUTPUTS</span></span>

### <span data-ttu-id="24677-166">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="24677-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="24677-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24677-167">NOTES</span></span>

## <span data-ttu-id="24677-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24677-168">RELATED LINKS</span></span>

[<span data-ttu-id="24677-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="24677-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="24677-170">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="24677-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="24677-171">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="24677-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


