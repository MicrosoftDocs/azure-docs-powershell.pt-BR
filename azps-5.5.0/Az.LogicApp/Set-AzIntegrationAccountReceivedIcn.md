---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113605"
---
# <span data-ttu-id="e4095-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="e4095-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="e4095-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4095-102">SYNOPSIS</span></span>
<span data-ttu-id="e4095-103">Atualiza a conta de integração recebida ICN (número de controle intercambiável) no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4095-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="e4095-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4095-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4095-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4095-105">DESCRIPTION</span></span>
<span data-ttu-id="e4095-106">O Set-AzIntegrationAccountGeneratedIcn cmdlet atualiza uma conta de integração existente recebida ICN (número de controle de troca troca) e retorna um objeto que representa o número de controle de troca recebido da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4095-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="e4095-107">Use este cmdlet para atualizar o status de processamento de mensagens de uma conta de integração recebida.</span><span class="sxs-lookup"><span data-stu-id="e4095-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="e4095-108">Você pode atualizar um número de controle intercambiável recebido de uma conta de integração especificando o nome da conta de integração, o nome do grupo de recursos, o nome do contrato, o valor do número de controle e o status de processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e4095-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="e4095-109">Não é possível criar uma nova conta de integração recebida com este comando.</span><span class="sxs-lookup"><span data-stu-id="e4095-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="e4095-110">Para usar os parâmetros dinâmicos, basta digitá-los no comando ou digitar um sinal de hífen(-) para indicar um nome de parâmetro e pressionar a tecla TAB repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e4095-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e4095-111">Se você perder um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="e4095-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="e4095-112">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores dos parâmetros de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="e4095-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="e4095-113">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem ser retornados</span><span class="sxs-lookup"><span data-stu-id="e4095-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="e4095-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4095-114">EXAMPLES</span></span>

### <span data-ttu-id="e4095-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4095-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="e4095-116">Esse comando atualiza a conta de integração recebida número do controle de troca X12 para um contrato de conta de integração específico e o valor com o status de processamento de mensagens falhou.</span><span class="sxs-lookup"><span data-stu-id="e4095-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="e4095-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4095-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="e4095-118">Esse comando atualiza a conta de integração que recebeu o número de controle de troca de Edifact para um contrato de conta de integração específico e um valor com o status de processamento de mensagens falhou.</span><span class="sxs-lookup"><span data-stu-id="e4095-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="e4095-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4095-119">PARAMETERS</span></span>

### <span data-ttu-id="e4095-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="e4095-120">-AgreementName</span></span>
<span data-ttu-id="e4095-121">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4095-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="e4095-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="e4095-122">-AgreementType</span></span>
<span data-ttu-id="e4095-123">O tipo de contrato de conta de integração (X12 ou Edifact).</span><span class="sxs-lookup"><span data-stu-id="e4095-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="e4095-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="e4095-124">-ControlNumberValue</span></span>
<span data-ttu-id="e4095-125">O valor de número do controle de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4095-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="e4095-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4095-126">-DefaultProfile</span></span>
<span data-ttu-id="e4095-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e4095-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4095-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="e4095-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="e4095-129">O status de processamento da mensagem recebida.</span><span class="sxs-lookup"><span data-stu-id="e4095-129">The received message processing status.</span></span>

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

### <span data-ttu-id="e4095-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4095-130">-Name</span></span>
<span data-ttu-id="e4095-131">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4095-131">The integration account name.</span></span>

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

### <span data-ttu-id="e4095-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4095-132">-ResourceGroupName</span></span>
<span data-ttu-id="e4095-133">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4095-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="e4095-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e4095-134">-Confirm</span></span>
<span data-ttu-id="e4095-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4095-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4095-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4095-136">-WhatIf</span></span>
<span data-ttu-id="e4095-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e4095-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4095-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4095-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4095-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4095-139">CommonParameters</span></span>
<span data-ttu-id="e4095-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4095-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4095-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4095-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4095-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4095-142">INPUTS</span></span>

### <span data-ttu-id="e4095-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e4095-143">System.String</span></span>

## <span data-ttu-id="e4095-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4095-144">OUTPUTS</span></span>

### <span data-ttu-id="e4095-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="e4095-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="e4095-146">Notas</span><span class="sxs-lookup"><span data-stu-id="e4095-146">NOTES</span></span>

## <span data-ttu-id="e4095-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4095-147">RELATED LINKS</span></span>

<span data-ttu-id="e4095-148">[Get-AzIntegrationAccountRecountIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountRecountIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="e4095-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
