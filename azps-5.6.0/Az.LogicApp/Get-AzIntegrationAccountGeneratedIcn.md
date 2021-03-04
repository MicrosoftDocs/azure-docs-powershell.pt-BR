---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b6bf2c126a1009d824ab8bae1ea2e2031459d876
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886462"
---
# <span data-ttu-id="97028-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="97028-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="97028-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97028-102">SYNOPSIS</span></span>
<span data-ttu-id="97028-103">Este cmdlet recupera o valor atual do número de controle de intercâmbio gerado por contrato.</span><span class="sxs-lookup"><span data-stu-id="97028-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="97028-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="97028-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97028-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="97028-105">DESCRIPTION</span></span>
<span data-ttu-id="97028-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para recuperar o valor atual do número de controle de intercâmbio gerado para gravar de volta um valor maior com Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="97028-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="97028-107">O número de controle de intercâmbio deve ser aumentado para evitar números de controle de intercâmbio duplicados para os números que ainda não puderam ser replicados para a região passiva quando o desastre aconteceu na região ativa.</span><span class="sxs-lookup"><span data-stu-id="97028-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="97028-108">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem retornar</span><span class="sxs-lookup"><span data-stu-id="97028-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="97028-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97028-109">EXAMPLES</span></span>

### <span data-ttu-id="97028-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97028-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="97028-111">Este comando obtém o número de controle de intercâmbio X12 gerado pela conta de integração pelo nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="97028-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="97028-112">Verifique se o contrato especificado é do tipo "X12"</span><span class="sxs-lookup"><span data-stu-id="97028-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="97028-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="97028-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="97028-114">Este comando obtém a conta de integração gerada número de controle de intercâmbio do Edifact pelo nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="97028-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="97028-115">Verifique se o contrato especificado é do tipo "Edifact"</span><span class="sxs-lookup"><span data-stu-id="97028-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="97028-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="97028-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="97028-117">Esse comando obtém todos os números de controle de intercâmbio X12 gerados pelo nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="97028-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="97028-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="97028-118">PARAMETERS</span></span>

### <span data-ttu-id="97028-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="97028-119">-AgreementName</span></span>
<span data-ttu-id="97028-120">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="97028-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="97028-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="97028-121">-AgreementType</span></span>
<span data-ttu-id="97028-122">O tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="97028-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="97028-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97028-123">-DefaultProfile</span></span>
<span data-ttu-id="97028-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="97028-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97028-125">-Name</span><span class="sxs-lookup"><span data-stu-id="97028-125">-Name</span></span>
<span data-ttu-id="97028-126">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="97028-126">The integration account name.</span></span>

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

### <span data-ttu-id="97028-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97028-127">-ResourceGroupName</span></span>
<span data-ttu-id="97028-128">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="97028-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="97028-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97028-129">CommonParameters</span></span>
<span data-ttu-id="97028-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97028-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97028-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97028-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97028-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97028-132">INPUTS</span></span>

### <span data-ttu-id="97028-133">System.String</span><span class="sxs-lookup"><span data-stu-id="97028-133">System.String</span></span>

## <span data-ttu-id="97028-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="97028-134">OUTPUTS</span></span>

### <span data-ttu-id="97028-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="97028-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="97028-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="97028-136">NOTES</span></span>

## <span data-ttu-id="97028-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97028-137">RELATED LINKS</span></span>

[<span data-ttu-id="97028-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="97028-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

