---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 5797aa1762ccc11f50486e5f932926fff21a0ee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430900"
---
# <span data-ttu-id="7beb6-101">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7beb6-101">Set-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="7beb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7beb6-102">SYNOPSIS</span></span>
<span data-ttu-id="7beb6-103">Modifica um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7beb6-103">Modifies an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7beb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7beb6-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7beb6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7beb6-105">DESCRIPTION</span></span>
<span data-ttu-id="7beb6-106">O cmdlet **set-AzureRmIntegrationAccountAgreement** modifica um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7beb6-106">The **Set-AzureRmIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="7beb6-107">Esse cmdlet retorna um objeto que representa o contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7beb6-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="7beb6-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="7beb6-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="7beb6-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="7beb6-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="7beb6-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="7beb6-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7beb6-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="7beb6-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7beb6-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7beb6-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7beb6-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="7beb6-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7beb6-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7beb6-114">EXAMPLES</span></span>

### <span data-ttu-id="7beb6-115">Exemplo 1: atualizar um contrato de conta de integração</span><span class="sxs-lookup"><span data-stu-id="7beb6-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="7beb6-116">Este comando atualiza um contrato de conta de integração no grupo de recursos do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="7beb6-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="7beb6-117">OS</span><span class="sxs-lookup"><span data-stu-id="7beb6-117">PARAMETERS</span></span>

### <span data-ttu-id="7beb6-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="7beb6-118">-AgreementContent</span></span>
<span data-ttu-id="7beb6-119">Especifica o conteúdo do contrato, no formato JSON (JavaScript Object Notation), para o contrato.</span><span class="sxs-lookup"><span data-stu-id="7beb6-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="7beb6-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="7beb6-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="7beb6-121">Especifica o caminho de arquivo do conteúdo do contrato para o contrato.</span><span class="sxs-lookup"><span data-stu-id="7beb6-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="7beb6-122">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="7beb6-122">-AgreementName</span></span>
<span data-ttu-id="7beb6-123">Especifica o nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7beb6-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="7beb6-124">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="7beb6-124">-AgreementType</span></span>
<span data-ttu-id="7beb6-125">Especifica o tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7beb6-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="7beb6-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7beb6-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7beb6-127">X12</span><span class="sxs-lookup"><span data-stu-id="7beb6-127">X12</span></span> 
- <span data-ttu-id="7beb6-128">AS2</span><span class="sxs-lookup"><span data-stu-id="7beb6-128">AS2</span></span>
- <span data-ttu-id="7beb6-129">Edifact</span><span class="sxs-lookup"><span data-stu-id="7beb6-129">Edifact</span></span>

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

### <span data-ttu-id="7beb6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7beb6-130">-DefaultProfile</span></span>
<span data-ttu-id="7beb6-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7beb6-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7beb6-132">-Force</span><span class="sxs-lookup"><span data-stu-id="7beb6-132">-Force</span></span>
<span data-ttu-id="7beb6-133">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7beb6-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7beb6-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="7beb6-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="7beb6-135">Especifica um nome qualificador de identidade de empresa para o parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="7beb6-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="7beb6-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="7beb6-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="7beb6-137">O contrato da conta de integração é um valor qualificador de identidade de convidado.</span><span class="sxs-lookup"><span data-stu-id="7beb6-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="7beb6-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="7beb6-138">-GuestPartner</span></span>
<span data-ttu-id="7beb6-139">Especifica o nome do parceiro convidado.</span><span class="sxs-lookup"><span data-stu-id="7beb6-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="7beb6-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="7beb6-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="7beb6-141">Especifica um nome qualificador de identidade de empresa para o parceiro do host.</span><span class="sxs-lookup"><span data-stu-id="7beb6-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="7beb6-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="7beb6-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="7beb6-143">O valor do qualificador de identidade de host do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7beb6-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="7beb6-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="7beb6-144">-HostPartner</span></span>
<span data-ttu-id="7beb6-145">Especifica o nome do parceiro do host.</span><span class="sxs-lookup"><span data-stu-id="7beb6-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="7beb6-146">-Metadados</span><span class="sxs-lookup"><span data-stu-id="7beb6-146">-Metadata</span></span>
<span data-ttu-id="7beb6-147">Especifica um objeto de metadados para o contrato.</span><span class="sxs-lookup"><span data-stu-id="7beb6-147">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="7beb6-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="7beb6-148">-Name</span></span>
<span data-ttu-id="7beb6-149">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7beb6-149">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="7beb6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7beb6-150">-ResourceGroupName</span></span>
<span data-ttu-id="7beb6-151">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7beb6-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7beb6-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7beb6-152">-Confirm</span></span>
<span data-ttu-id="7beb6-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7beb6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7beb6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7beb6-154">-WhatIf</span></span>
<span data-ttu-id="7beb6-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7beb6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7beb6-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7beb6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7beb6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7beb6-157">CommonParameters</span></span>
<span data-ttu-id="7beb6-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7beb6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7beb6-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7beb6-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7beb6-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7beb6-160">INPUTS</span></span>

### <span data-ttu-id="7beb6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7beb6-161">System.String</span></span>

## <span data-ttu-id="7beb6-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7beb6-162">OUTPUTS</span></span>

### <span data-ttu-id="7beb6-163">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7beb6-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="7beb6-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7beb6-164">NOTES</span></span>

## <span data-ttu-id="7beb6-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7beb6-165">RELATED LINKS</span></span>

[<span data-ttu-id="7beb6-166">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7beb6-166">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="7beb6-167">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7beb6-167">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="7beb6-168">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7beb6-168">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)


