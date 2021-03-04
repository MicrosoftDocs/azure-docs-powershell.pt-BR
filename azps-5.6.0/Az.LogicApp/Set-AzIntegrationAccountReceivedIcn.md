---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 076679499cf64100bcded5a29e7bc158a81423ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887502"
---
# <span data-ttu-id="1ba4f-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="1ba4f-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="1ba4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ba4f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba4f-103">Atualiza a conta de integração recebida ICN (número de controle de intercâmbio) no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="1ba4f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1ba4f-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ba4f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ba4f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba4f-106">O cmdlet Set-AzIntegrationAccountGeneratedIcn atualiza uma conta de integração existente recebeu o número de controle de intercâmbio (ICN) e retorna um objeto que representa a conta de integração recebida número de controle de intercâmbio.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="1ba4f-107">Use este cmdlet para atualizar o status de processamento de mensagens de uma conta de integração recebida do número de controle de intercâmbio.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="1ba4f-108">Você pode atualizar uma conta de integração recebida número de controle de intercâmbio especificando o nome da conta de integração, o nome do grupo de recursos, o nome do contrato, o valor do número de controle e o status de processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="1ba4f-109">Não é possível criar uma nova conta de integração recebida com este comando.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="1ba4f-110">Para usar os parâmetros dinâmicos, digite-os no comando ou digite um sinal de hífen(-) para indicar um nome de parâmetro e pressione a tecla TAB repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1ba4f-111">Se você perder um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="1ba4f-112">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores de parâmetro de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="1ba4f-113">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem retornar</span><span class="sxs-lookup"><span data-stu-id="1ba4f-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="1ba4f-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ba4f-114">EXAMPLES</span></span>

### <span data-ttu-id="1ba4f-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ba4f-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="1ba4f-116">Este comando atualiza a conta de integração recebida número de controle de intercâmbio X12 para um contrato de conta de integração específico e o valor com o status de processamento de mensagens falhou.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="1ba4f-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1ba4f-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="1ba4f-118">Este comando atualiza a conta de integração recebida número de controle de troca de Edifact para um contrato de conta de integração específico e o valor com o status de processamento de mensagens falhou.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="1ba4f-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1ba4f-119">PARAMETERS</span></span>

### <span data-ttu-id="1ba4f-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="1ba4f-120">-AgreementName</span></span>
<span data-ttu-id="1ba4f-121">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="1ba4f-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="1ba4f-122">-AgreementType</span></span>
<span data-ttu-id="1ba4f-123">O tipo de contrato de conta de integração (X12 ou Edifact).</span><span class="sxs-lookup"><span data-stu-id="1ba4f-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="1ba4f-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="1ba4f-124">-ControlNumberValue</span></span>
<span data-ttu-id="1ba4f-125">O valor do número de controle da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="1ba4f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba4f-126">-DefaultProfile</span></span>
<span data-ttu-id="1ba4f-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1ba4f-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ba4f-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="1ba4f-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="1ba4f-129">O status de processamento de mensagens recebidas.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-129">The received message processing status.</span></span>

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

### <span data-ttu-id="1ba4f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="1ba4f-130">-Name</span></span>
<span data-ttu-id="1ba4f-131">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-131">The integration account name.</span></span>

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

### <span data-ttu-id="1ba4f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba4f-132">-ResourceGroupName</span></span>
<span data-ttu-id="1ba4f-133">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="1ba4f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ba4f-134">-Confirm</span></span>
<span data-ttu-id="1ba4f-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba4f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba4f-136">-WhatIf</span></span>
<span data-ttu-id="1ba4f-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba4f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba4f-139">CommonParameters</span></span>
<span data-ttu-id="1ba4f-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba4f-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba4f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba4f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ba4f-142">INPUTS</span></span>

### <span data-ttu-id="1ba4f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1ba4f-143">System.String</span></span>

## <span data-ttu-id="1ba4f-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1ba4f-144">OUTPUTS</span></span>

### <span data-ttu-id="1ba4f-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="1ba4f-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="1ba4f-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="1ba4f-146">NOTES</span></span>

## <span data-ttu-id="1ba4f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ba4f-147">RELATED LINKS</span></span>

<span data-ttu-id="1ba4f-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="1ba4f-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
