---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 2a80173900c0faf062c3d4ba0c0a3b2029737bcf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114471"
---
# <span data-ttu-id="cf3c5-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="cf3c5-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="cf3c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf3c5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3c5-103">Esse cmdlet Remove um número específico de controle de intercâmbio recebido por acordo e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="cf3c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf3c5-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf3c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf3c5-105">DESCRIPTION</span></span>
<span data-ttu-id="cf3c5-106">Este cmdlet se destina a ser usado em cenários de recuperação de desastres para remover um número de controle de intercâmbio recebido da conta de integração para que o conector B2B possa processar novamente a mensagem quando a detecção de número duplicado estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="cf3c5-107">Em raras ocasiões, o número de controle de intercâmbio recebido pode ser reservado logo antes de um desastre e antes de o conector B2B rejeitar o intercâmbio como errado.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="cf3c5-108">Em tais ocasiões, a operação pode querer habilitar o site de recuperação para processar novamente o mesmo intercâmbio após a correção da carga.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="cf3c5-109">Forneça o parâmetro "-Agreementtype" para especificar se os números de controle X12 ou EDIFACT a serem retornados</span><span class="sxs-lookup"><span data-stu-id="cf3c5-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="cf3c5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf3c5-110">EXAMPLES</span></span>

### <span data-ttu-id="cf3c5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf3c5-111">Example 1</span></span>
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

<span data-ttu-id="cf3c5-112">Tenta obter um número de controle de troca X12 recebido que o conteúdo não está em um formato válido.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="cf3c5-113">Remove o número de controle de troca X12 recebido.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="cf3c5-114">Confirma que o número de controle de intercâmbio recebido X12 foi removido tentando recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="cf3c5-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cf3c5-115">Example 2</span></span>
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

<span data-ttu-id="cf3c5-116">Tenta obter um número de controle de troca EDIFACT recebido que o conteúdo não está em um formato válido.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="cf3c5-117">Remove o número de controle de troca EDIFACT recebido.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="cf3c5-118">Confirma que o número de controle de intercâmbio recebido EDIFACT foi removido tentando recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="cf3c5-119">OS</span><span class="sxs-lookup"><span data-stu-id="cf3c5-119">PARAMETERS</span></span>

### <span data-ttu-id="cf3c5-120">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="cf3c5-120">-AgreementName</span></span>
<span data-ttu-id="cf3c5-121">O nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="cf3c5-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="cf3c5-122">-AgreementType</span></span>
<span data-ttu-id="cf3c5-123">O tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="cf3c5-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="cf3c5-124">-ControlNumberValue</span></span>
<span data-ttu-id="cf3c5-125">O valor de número de controle da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="cf3c5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3c5-126">-DefaultProfile</span></span>
<span data-ttu-id="cf3c5-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cf3c5-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf3c5-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf3c5-128">-Name</span></span>
<span data-ttu-id="cf3c5-129">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-129">The integration account name.</span></span>

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

### <span data-ttu-id="cf3c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf3c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="cf3c5-131">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="cf3c5-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf3c5-132">-Confirm</span></span>
<span data-ttu-id="cf3c5-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf3c5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf3c5-134">-WhatIf</span></span>
<span data-ttu-id="cf3c5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf3c5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf3c5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3c5-137">CommonParameters</span></span>
<span data-ttu-id="cf3c5-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3c5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3c5-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf3c5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3c5-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf3c5-140">INPUTS</span></span>

### <span data-ttu-id="cf3c5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cf3c5-141">System.String</span></span>

## <span data-ttu-id="cf3c5-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf3c5-142">OUTPUTS</span></span>

### <span data-ttu-id="cf3c5-143">System. void</span><span class="sxs-lookup"><span data-stu-id="cf3c5-143">System.Void</span></span>

## <span data-ttu-id="cf3c5-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf3c5-144">NOTES</span></span>

## <span data-ttu-id="cf3c5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf3c5-145">RELATED LINKS</span></span>

<span data-ttu-id="cf3c5-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="cf3c5-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

