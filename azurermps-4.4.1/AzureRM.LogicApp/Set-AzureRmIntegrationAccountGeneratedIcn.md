---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: dd133b2a0d982cb2017651ff86dcf3a846009c2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609651"
---
# <span data-ttu-id="e4063-101">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="e4063-101">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="e4063-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4063-102">SYNOPSIS</span></span>
<span data-ttu-id="e4063-103">Atualiza a conta de integração do número de controle de intercâmbio (ICN) gerado no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4063-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4063-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4063-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4063-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4063-105">DESCRIPTION</span></span>
<span data-ttu-id="e4063-106">O cmdlet Set-AzureRmIntegrationAccountGeneratedIcn atualiza uma conta de integração existente que gerou o ICN (Interchange Control Number) e retorna um objeto que representa a conta de integração que gerou o número de controle de intercâmbio.</span><span class="sxs-lookup"><span data-stu-id="e4063-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="e4063-107">Use esse cmdlet para atualizar uma conta de integração do número de controle de intercâmbio gerado.</span><span class="sxs-lookup"><span data-stu-id="e4063-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="e4063-108">Você pode atualizar uma conta de integração do número de controle do intercâmbio gerado especificando o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="e4063-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="e4063-109">Você não pode criar uma nova conta de integração do número de controle de intercâmbio gerado com este comando.</span><span class="sxs-lookup"><span data-stu-id="e4063-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="e4063-110">Para usar os parâmetros dinâmicos, basta digitá-los no comando ou digitar um sinal de hífen (-) para indicar um nome de parâmetro e, em seguida, pressionar a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e4063-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e4063-111">Se você perder um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="e4063-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="e4063-112">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="e4063-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="e4063-113">Forneça o parâmetro "-Agreementtype" para especificar se os números de controle X12 ou EDIFACT a serem retornados</span><span class="sxs-lookup"><span data-stu-id="e4063-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="e4063-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4063-114">EXAMPLES</span></span>

### <span data-ttu-id="e4063-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4063-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="e4063-116">Esse comando obtém a conta de integração gerada X12 o número do controle de troca para um contrato de conta de integração específico, aumentar o valor de 100 e gravar novamente o valor atualizado.</span><span class="sxs-lookup"><span data-stu-id="e4063-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="e4063-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4063-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="e4063-118">Esse comando obtém a conta de integração gerada EdifactIntegrationAccountAgreement o número do controle de troca para um contrato de conta de integração específico, aumentar o valor de 100 e gravar novamente o valor atualizado.</span><span class="sxs-lookup"><span data-stu-id="e4063-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="e4063-119">OS</span><span class="sxs-lookup"><span data-stu-id="e4063-119">PARAMETERS</span></span>

### <span data-ttu-id="e4063-120">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="e4063-120">-AgreementName</span></span>
<span data-ttu-id="e4063-121">O nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4063-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="e4063-122">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="e4063-122">-ControlNumber</span></span>
<span data-ttu-id="e4063-123">O número de controle gerado novo valor.</span><span class="sxs-lookup"><span data-stu-id="e4063-123">The generated control number new value.</span></span>

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

### <span data-ttu-id="e4063-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4063-124">-Name</span></span>
<span data-ttu-id="e4063-125">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4063-125">The integration account name.</span></span>

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

### <span data-ttu-id="e4063-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4063-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4063-127">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4063-127">The integration account resource group name.</span></span>

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

### <span data-ttu-id="e4063-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4063-128">-Confirm</span></span>
<span data-ttu-id="e4063-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4063-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4063-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4063-130">-WhatIf</span></span>
<span data-ttu-id="e4063-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4063-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4063-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4063-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4063-133">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="e4063-133">-AgreementType</span></span>
<span data-ttu-id="e4063-134">O tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e4063-134">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4063-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4063-135">-DefaultProfile</span></span>
<span data-ttu-id="e4063-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4063-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4063-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4063-137">CommonParameters</span></span>
<span data-ttu-id="e4063-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4063-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4063-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4063-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4063-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4063-140">INPUTS</span></span>

### <span data-ttu-id="e4063-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e4063-141">System.String</span></span>

## <span data-ttu-id="e4063-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4063-142">OUTPUTS</span></span>

### <span data-ttu-id="e4063-143">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="e4063-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="e4063-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4063-144">NOTES</span></span>

## <span data-ttu-id="e4063-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4063-145">RELATED LINKS</span></span>

[<span data-ttu-id="e4063-146">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="e4063-146">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Get-AzureRmIntegrationAccountGeneratedIcn.md)

