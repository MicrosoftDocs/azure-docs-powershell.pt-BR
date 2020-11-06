---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 4f9beaec4a665871db8bf5dc089deb02617ee8fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429757"
---
# <span data-ttu-id="89a73-101">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="89a73-101">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="89a73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89a73-102">SYNOPSIS</span></span>
<span data-ttu-id="89a73-103">Esse cmdlet Remove um número específico de controle de intercâmbio recebido por acordo e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="89a73-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89a73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89a73-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89a73-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89a73-105">DESCRIPTION</span></span>
<span data-ttu-id="89a73-106">Este cmdlet se destina a ser usado em cenários de recuperação de desastres para remover um número de controle de intercâmbio recebido da conta de integração para que o conector B2B possa processar novamente a mensagem quando a detecção de número duplicado estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="89a73-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="89a73-107">Em raras ocasiões, o número de controle de intercâmbio recebido pode ser reservado logo antes de um desastre e antes de o conector B2B rejeitar o intercâmbio como errado.</span><span class="sxs-lookup"><span data-stu-id="89a73-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="89a73-108">Em tais ocasiões, a operação pode querer habilitar o site de recuperação para processar novamente o mesmo intercâmbio após a correção da carga.</span><span class="sxs-lookup"><span data-stu-id="89a73-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="89a73-109">Forneça o parâmetro "-Agreementtype" para especificar se os números de controle X12 ou EDIFACT a serem retornados</span><span class="sxs-lookup"><span data-stu-id="89a73-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="89a73-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89a73-110">EXAMPLES</span></span>

### <span data-ttu-id="89a73-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89a73-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="89a73-112">Tenta obter um número de controle de troca X12 recebido que o conteúdo não está em um formato válido.</span><span class="sxs-lookup"><span data-stu-id="89a73-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="89a73-113">Remove o número de controle de troca X12 recebido.</span><span class="sxs-lookup"><span data-stu-id="89a73-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="89a73-114">Confirma que o número de controle de intercâmbio recebido X12 foi removido tentando recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="89a73-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="89a73-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="89a73-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="89a73-116">Tenta obter um número de controle de troca EDIFACT recebido que o conteúdo não está em um formato válido.</span><span class="sxs-lookup"><span data-stu-id="89a73-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="89a73-117">Remove o número de controle de troca EDIFACT recebido.</span><span class="sxs-lookup"><span data-stu-id="89a73-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="89a73-118">Confirma que o número de controle de intercâmbio recebido EDIFACT foi removido tentando recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="89a73-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="89a73-119">OS</span><span class="sxs-lookup"><span data-stu-id="89a73-119">PARAMETERS</span></span>

### <span data-ttu-id="89a73-120">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="89a73-120">-AgreementName</span></span>
<span data-ttu-id="89a73-121">O nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="89a73-121">The integration account agreement name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a73-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="89a73-122">-AgreementType</span></span>
<span data-ttu-id="89a73-123">O tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="89a73-123">The integration account agreement type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a73-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="89a73-124">-ControlNumberValue</span></span>
<span data-ttu-id="89a73-125">O valor de número de controle da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="89a73-125">The integration account control number value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a73-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a73-126">-DefaultProfile</span></span>
<span data-ttu-id="89a73-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="89a73-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a73-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="89a73-128">-Name</span></span>
<span data-ttu-id="89a73-129">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="89a73-129">The integration account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a73-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89a73-130">-ResourceGroupName</span></span>
<span data-ttu-id="89a73-131">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="89a73-131">The integration account resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89a73-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89a73-132">-Confirm</span></span>
<span data-ttu-id="89a73-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89a73-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a73-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a73-134">-WhatIf</span></span>
<span data-ttu-id="89a73-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89a73-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89a73-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89a73-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a73-137">CommonParameters</span></span>
<span data-ttu-id="89a73-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89a73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a73-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a73-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a73-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89a73-140">INPUTS</span></span>

### <span data-ttu-id="89a73-141">System. String</span><span class="sxs-lookup"><span data-stu-id="89a73-141">System.String</span></span>

## <span data-ttu-id="89a73-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89a73-142">OUTPUTS</span></span>

### <span data-ttu-id="89a73-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="89a73-143">System.Object</span></span>

## <span data-ttu-id="89a73-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89a73-144">NOTES</span></span>

## <span data-ttu-id="89a73-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89a73-145">RELATED LINKS</span></span>

<span data-ttu-id="89a73-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="89a73-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span></span>

