---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 94cb9c54752b29da68beefa713894fd77a385b45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596006"
---
# <span data-ttu-id="2f0c1-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="2f0c1-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="2f0c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f0c1-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0c1-103">Atualiza a conta de integração número de controle de troca recebido (ICN) no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="2f0c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f0c1-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f0c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f0c1-105">DESCRIPTION</span></span>
<span data-ttu-id="2f0c1-106">O cmdlet Set-AzIntegrationAccountGeneratedIcn atualiza uma conta de integração existente que recebeu o número de controle de troca (ICN) e retorna um objeto que representa a conta de integração do número de controle de intercâmbio recebido.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="2f0c1-107">Use esse cmdlet para atualizar uma conta de integração que recebeu o status de processamento de mensagem do número do controle de troca.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="2f0c1-108">Você pode atualizar uma conta de integração que recebeu um número de controle do intercâmbio especificando o nome da conta de integração, o nome do grupo de recursos, o nome do contrato, o valor do número do controle e o status do processamento</span><span class="sxs-lookup"><span data-stu-id="2f0c1-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="2f0c1-109">Você não pode criar uma nova conta de integração que recebeu um número de controle de troca com este comando.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="2f0c1-110">Para usar os parâmetros dinâmicos, basta digitá-los no comando ou digitar um sinal de hífen (-) para indicar um nome de parâmetro e, em seguida, pressionar a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2f0c1-111">Se você perder um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="2f0c1-112">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="2f0c1-113">Forneça o parâmetro "-Agreementtype" para especificar se os números de controle X12 ou EDIFACT a serem retornados</span><span class="sxs-lookup"><span data-stu-id="2f0c1-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="2f0c1-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f0c1-114">EXAMPLES</span></span>

### <span data-ttu-id="2f0c1-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f0c1-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="2f0c1-116">Este comando atualiza a conta de integração recebida X12 número de controle de troca de um determinado contrato de conta de integração e valor com o status de processamento de mensagens falhou.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="2f0c1-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2f0c1-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="2f0c1-118">Este comando atualiza a conta de integração recebida EDIFACT número de controle de troca de um determinado contrato de conta de integração e valor com o status de processamento de mensagens falhou.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="2f0c1-119">OS</span><span class="sxs-lookup"><span data-stu-id="2f0c1-119">PARAMETERS</span></span>

### <span data-ttu-id="2f0c1-120">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="2f0c1-120">-AgreementName</span></span>
<span data-ttu-id="2f0c1-121">O nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="2f0c1-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="2f0c1-122">-AgreementType</span></span>
<span data-ttu-id="2f0c1-123">O tipo de contrato da conta de integração (X12 ou EDIFACT).</span><span class="sxs-lookup"><span data-stu-id="2f0c1-123">The integration account agreement type (X12 or Edifact).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0c1-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="2f0c1-124">-ControlNumberValue</span></span>
<span data-ttu-id="2f0c1-125">O valor de número de controle da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="2f0c1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0c1-126">-DefaultProfile</span></span>
<span data-ttu-id="2f0c1-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2f0c1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f0c1-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="2f0c1-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="2f0c1-129">O status de processamento de mensagens recebidas.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0c1-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f0c1-130">-Name</span></span>
<span data-ttu-id="2f0c1-131">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-131">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0c1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0c1-132">-ResourceGroupName</span></span>
<span data-ttu-id="2f0c1-133">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="2f0c1-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f0c1-134">-Confirm</span></span>
<span data-ttu-id="2f0c1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f0c1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0c1-136">-WhatIf</span></span>
<span data-ttu-id="2f0c1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f0c1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f0c1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0c1-139">CommonParameters</span></span>
<span data-ttu-id="2f0c1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f0c1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0c1-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f0c1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0c1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f0c1-142">INPUTS</span></span>

### <span data-ttu-id="2f0c1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2f0c1-143">System.String</span></span>

## <span data-ttu-id="2f0c1-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f0c1-144">OUTPUTS</span></span>

### <span data-ttu-id="2f0c1-145">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="2f0c1-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="2f0c1-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f0c1-146">NOTES</span></span>

## <span data-ttu-id="2f0c1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f0c1-147">RELATED LINKS</span></span>

<span data-ttu-id="2f0c1-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="2f0c1-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
