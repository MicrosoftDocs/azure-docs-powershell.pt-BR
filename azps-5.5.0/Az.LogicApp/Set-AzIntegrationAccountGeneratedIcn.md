---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: fa02d7ffc23706564b8b6fe118f12525829b27f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113609"
---
# <span data-ttu-id="4c62c-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="4c62c-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="4c62c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c62c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c62c-103">Atualiza o número de controle de troca gerado pela conta de integração (ICN) no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c62c-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="4c62c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c62c-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c62c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c62c-105">DESCRIPTION</span></span>
<span data-ttu-id="4c62c-106">O cmdlet Set-AzIntegrationAccountGeneratedIcn atualiza uma conta de integração existente gerada por um número de controle de troca (ICN) e retorna um objeto que representa o número de controle de troca gerado pela conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4c62c-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="4c62c-107">Use este cmdlet para atualizar um número de controle de troca gerado por uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4c62c-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="4c62c-108">Você pode atualizar um número de controle de troca gerado por uma conta de integração especificando o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="4c62c-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="4c62c-109">Você não pode criar uma nova conta de integração gerada número de controle de troca com esse comando.</span><span class="sxs-lookup"><span data-stu-id="4c62c-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="4c62c-110">Para usar os parâmetros dinâmicos, basta digitá-los no comando ou digitar um sinal de hífen(-) para indicar um nome de parâmetro e pressionar a tecla TAB repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4c62c-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4c62c-111">Se você perder um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="4c62c-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="4c62c-112">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores dos parâmetros de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="4c62c-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="4c62c-113">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem ser retornados</span><span class="sxs-lookup"><span data-stu-id="4c62c-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="4c62c-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c62c-114">EXAMPLES</span></span>

### <span data-ttu-id="4c62c-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c62c-115">Example 1</span></span>
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

<span data-ttu-id="4c62c-116">Esse comando obtém a conta de integração gerada X12 número de controle de troca para um contrato de conta de integração específico, aumenta seu valor em 100 e, em seguida, grava o valor atualizado.</span><span class="sxs-lookup"><span data-stu-id="4c62c-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="4c62c-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4c62c-117">Example 2</span></span>
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

<span data-ttu-id="4c62c-118">Esse comando obtém a conta de integração gerada EdifactIntegrationAccountAgreement de um contrato de conta de integração específico, aumenta seu valor em 100 e, em seguida, grava o valor atualizado.</span><span class="sxs-lookup"><span data-stu-id="4c62c-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="4c62c-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c62c-119">PARAMETERS</span></span>

### <span data-ttu-id="4c62c-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="4c62c-120">-AgreementName</span></span>
<span data-ttu-id="4c62c-121">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4c62c-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="4c62c-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="4c62c-122">-AgreementType</span></span>
<span data-ttu-id="4c62c-123">O tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4c62c-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="4c62c-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="4c62c-124">-ControlNumber</span></span>
<span data-ttu-id="4c62c-125">O novo valor de número de controle gerado.</span><span class="sxs-lookup"><span data-stu-id="4c62c-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="4c62c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c62c-126">-DefaultProfile</span></span>
<span data-ttu-id="4c62c-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4c62c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c62c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c62c-128">-Name</span></span>
<span data-ttu-id="4c62c-129">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4c62c-129">The integration account name.</span></span>

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

### <span data-ttu-id="4c62c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c62c-130">-ResourceGroupName</span></span>
<span data-ttu-id="4c62c-131">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4c62c-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="4c62c-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4c62c-132">-Confirm</span></span>
<span data-ttu-id="4c62c-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c62c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c62c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c62c-134">-WhatIf</span></span>
<span data-ttu-id="4c62c-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4c62c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c62c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c62c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c62c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c62c-137">CommonParameters</span></span>
<span data-ttu-id="4c62c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c62c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c62c-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c62c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c62c-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="4c62c-140">INPUTS</span></span>

### <span data-ttu-id="4c62c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4c62c-141">System.String</span></span>

## <span data-ttu-id="4c62c-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="4c62c-142">OUTPUTS</span></span>

### <span data-ttu-id="4c62c-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="4c62c-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="4c62c-144">Notas</span><span class="sxs-lookup"><span data-stu-id="4c62c-144">NOTES</span></span>

## <span data-ttu-id="4c62c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c62c-145">RELATED LINKS</span></span>

[<span data-ttu-id="4c62c-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="4c62c-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

