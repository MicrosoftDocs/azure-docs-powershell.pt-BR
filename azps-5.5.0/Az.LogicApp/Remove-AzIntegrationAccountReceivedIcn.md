---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 2a80173900c0faf062c3d4ba0c0a3b2029737bcf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113610"
---
# <span data-ttu-id="c2cca-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c2cca-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="c2cca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2cca-102">SYNOPSIS</span></span>
<span data-ttu-id="c2cca-103">Este cmdlet remove um número de controle de troca de troca recebido específico por contrato e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="c2cca-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="c2cca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2cca-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2cca-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2cca-105">DESCRIPTION</span></span>
<span data-ttu-id="c2cca-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para remover um número de controle de troca recebido da conta de integração para que o conector B2B possa processar novamente a mensagem quando a detecção de número duplicada estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="c2cca-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="c2cca-107">Em raras ocasiões, o número do controle de troca recebido pode ser reservado logo antes de um desastre e antes que o conector B2B rejeite a troca como erronea.</span><span class="sxs-lookup"><span data-stu-id="c2cca-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="c2cca-108">Nesses casos, a operação pode permitir que o site de recuperação processe novamente a mesma troca após a correção da sua carga.</span><span class="sxs-lookup"><span data-stu-id="c2cca-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="c2cca-109">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem ser retornados</span><span class="sxs-lookup"><span data-stu-id="c2cca-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="c2cca-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2cca-110">EXAMPLES</span></span>

### <span data-ttu-id="c2cca-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2cca-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="c2cca-112">Tenta obter um número de controle de troca X12 recebido que o conteúdo não está em um formato válido.</span><span class="sxs-lookup"><span data-stu-id="c2cca-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="c2cca-113">Remove o número de controle de troca X12 recebido.</span><span class="sxs-lookup"><span data-stu-id="c2cca-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="c2cca-114">Confirma que o número do controle de troca de X12 recebido foi removido tentando obter novamente.</span><span class="sxs-lookup"><span data-stu-id="c2cca-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="c2cca-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c2cca-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="c2cca-116">Tenta obter um número de controle de troca de Edifact recebido que o conteúdo não está em um formato válido.</span><span class="sxs-lookup"><span data-stu-id="c2cca-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="c2cca-117">Remove o número de controle de troca de Edifact recebido.</span><span class="sxs-lookup"><span data-stu-id="c2cca-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="c2cca-118">Confirma que o número de controle de troca de Edifact recebido foi removido tentando obter novamente.</span><span class="sxs-lookup"><span data-stu-id="c2cca-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="c2cca-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2cca-119">PARAMETERS</span></span>

### <span data-ttu-id="c2cca-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="c2cca-120">-AgreementName</span></span>
<span data-ttu-id="c2cca-121">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c2cca-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="c2cca-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="c2cca-122">-AgreementType</span></span>
<span data-ttu-id="c2cca-123">O tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c2cca-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="c2cca-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="c2cca-124">-ControlNumberValue</span></span>
<span data-ttu-id="c2cca-125">O valor de número do controle de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c2cca-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="c2cca-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2cca-126">-DefaultProfile</span></span>
<span data-ttu-id="c2cca-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c2cca-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2cca-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2cca-128">-Name</span></span>
<span data-ttu-id="c2cca-129">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c2cca-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cca-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2cca-130">-ResourceGroupName</span></span>
<span data-ttu-id="c2cca-131">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c2cca-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="c2cca-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c2cca-132">-Confirm</span></span>
<span data-ttu-id="c2cca-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2cca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2cca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2cca-134">-WhatIf</span></span>
<span data-ttu-id="c2cca-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c2cca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2cca-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2cca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2cca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cca-137">CommonParameters</span></span>
<span data-ttu-id="c2cca-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2cca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cca-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2cca-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cca-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="c2cca-140">INPUTS</span></span>

### <span data-ttu-id="c2cca-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c2cca-141">System.String</span></span>

## <span data-ttu-id="c2cca-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="c2cca-142">OUTPUTS</span></span>

### <span data-ttu-id="c2cca-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="c2cca-143">System.Void</span></span>

## <span data-ttu-id="c2cca-144">Notas</span><span class="sxs-lookup"><span data-stu-id="c2cca-144">NOTES</span></span>

## <span data-ttu-id="c2cca-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2cca-145">RELATED LINKS</span></span>

<span data-ttu-id="c2cca-146">[Get-AzIntegrationAccountRecountIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountRecountIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="c2cca-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

