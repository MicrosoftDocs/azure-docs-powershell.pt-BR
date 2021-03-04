---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4c91ced490226901a45e0eacb7caa204daa20558
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888487"
---
# <span data-ttu-id="0c7b5-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="0c7b5-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="0c7b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7b5-103">Atualiza o número de controle de intercâmbio gerado pela conta de integração (ICN) no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="0c7b5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c7b5-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c7b5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c7b5-105">DESCRIPTION</span></span>
<span data-ttu-id="0c7b5-106">O cmdlet Set-AzIntegrationAccountGeneratedIcn atualiza uma conta de integração existente gerada pelo ICN (número de controle de intercâmbio) e retorna um objeto que representa o número de controle de intercâmbio gerado pela conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="0c7b5-107">Use este cmdlet para atualizar um número de controle de intercâmbio gerado por conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="0c7b5-108">Você pode atualizar um número de controle de intercâmbio gerado por conta de integração especificando o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="0c7b5-109">Não é possível criar uma nova conta de integração gerada pelo número de controle de intercâmbio com este comando.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="0c7b5-110">Para usar os parâmetros dinâmicos, digite-os no comando ou digite um sinal de hífen(-) para indicar um nome de parâmetro e pressione a tecla TAB repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0c7b5-111">Se você perder um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="0c7b5-112">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores de parâmetro de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="0c7b5-113">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem retornar</span><span class="sxs-lookup"><span data-stu-id="0c7b5-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="0c7b5-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c7b5-114">EXAMPLES</span></span>

### <span data-ttu-id="0c7b5-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c7b5-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="0c7b5-116">Esse comando obtém o número de controle de intercâmbio X12 gerado pela conta de integração para um contrato de conta de integração específico, aumenta seu valor em 100 e grava de volta o valor atualizado.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="0c7b5-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0c7b5-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="0c7b5-118">Este comando obtém a conta de integração gerada EdifactIntegrationAccountAgreement número de controle de intercâmbio para um contrato de conta de integração específico, aumenta seu valor em 100 e grava novamente o valor atualizado.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="0c7b5-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c7b5-119">PARAMETERS</span></span>

### <span data-ttu-id="0c7b5-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="0c7b5-120">-AgreementName</span></span>
<span data-ttu-id="0c7b5-121">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="0c7b5-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="0c7b5-122">-AgreementType</span></span>
<span data-ttu-id="0c7b5-123">O tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="0c7b5-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="0c7b5-124">-ControlNumber</span></span>
<span data-ttu-id="0c7b5-125">O novo valor do número de controle gerado.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="0c7b5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7b5-126">-DefaultProfile</span></span>
<span data-ttu-id="0c7b5-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0c7b5-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c7b5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0c7b5-128">-Name</span></span>
<span data-ttu-id="0c7b5-129">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-129">The integration account name.</span></span>

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

### <span data-ttu-id="0c7b5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7b5-130">-ResourceGroupName</span></span>
<span data-ttu-id="0c7b5-131">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="0c7b5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c7b5-132">-Confirm</span></span>
<span data-ttu-id="0c7b5-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c7b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c7b5-134">-WhatIf</span></span>
<span data-ttu-id="0c7b5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c7b5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c7b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7b5-137">CommonParameters</span></span>
<span data-ttu-id="0c7b5-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7b5-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c7b5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7b5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c7b5-140">INPUTS</span></span>

### <span data-ttu-id="0c7b5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0c7b5-141">System.String</span></span>

## <span data-ttu-id="0c7b5-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c7b5-142">OUTPUTS</span></span>

### <span data-ttu-id="0c7b5-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="0c7b5-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="0c7b5-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c7b5-144">NOTES</span></span>

## <span data-ttu-id="0c7b5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c7b5-145">RELATED LINKS</span></span>

[<span data-ttu-id="0c7b5-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="0c7b5-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

