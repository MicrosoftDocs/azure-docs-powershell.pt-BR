---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111815"
---
# <span data-ttu-id="63174-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="63174-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="63174-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63174-102">SYNOPSIS</span></span>
<span data-ttu-id="63174-103">Este cmdlet recupera o valor atual do número de controle de troca gerado por contrato.</span><span class="sxs-lookup"><span data-stu-id="63174-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="63174-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63174-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63174-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="63174-105">DESCRIPTION</span></span>
<span data-ttu-id="63174-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para recuperar o valor atual do número de controle de intercambiamento gerado, de modo a anotar um valor aumentado com Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="63174-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="63174-107">O número do controle de troca deve ser aumentado para evitar números de controle de troca duplicados para os números que ainda não puderam ser replicados para a região passiva quando o desastre aconteceu na região ativa.</span><span class="sxs-lookup"><span data-stu-id="63174-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="63174-108">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem ser retornados</span><span class="sxs-lookup"><span data-stu-id="63174-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="63174-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63174-109">EXAMPLES</span></span>

### <span data-ttu-id="63174-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63174-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="63174-111">Esse comando obtém a conta de integração gerada X12 número do controle de troca por nome de contrato.</span><span class="sxs-lookup"><span data-stu-id="63174-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="63174-112">Verifique se o contrato especificado é do tipo "X12"</span><span class="sxs-lookup"><span data-stu-id="63174-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="63174-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="63174-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="63174-114">Esse comando obtém o número de controle de troca gerado pela conta de integração Edifact por nome de contrato.</span><span class="sxs-lookup"><span data-stu-id="63174-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="63174-115">Certifique-se de que o contrato especificado seja do tipo "Edifact"</span><span class="sxs-lookup"><span data-stu-id="63174-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="63174-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="63174-116">Example 3</span></span>
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

<span data-ttu-id="63174-117">Esse comando obtém todos os números de controle de troca X12 gerados pelo nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="63174-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="63174-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63174-118">PARAMETERS</span></span>

### <span data-ttu-id="63174-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="63174-119">-AgreementName</span></span>
<span data-ttu-id="63174-120">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="63174-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="63174-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="63174-121">-AgreementType</span></span>
<span data-ttu-id="63174-122">O tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="63174-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="63174-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63174-123">-DefaultProfile</span></span>
<span data-ttu-id="63174-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="63174-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63174-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="63174-125">-Name</span></span>
<span data-ttu-id="63174-126">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="63174-126">The integration account name.</span></span>

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

### <span data-ttu-id="63174-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63174-127">-ResourceGroupName</span></span>
<span data-ttu-id="63174-128">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="63174-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="63174-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63174-129">CommonParameters</span></span>
<span data-ttu-id="63174-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63174-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63174-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63174-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63174-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="63174-132">INPUTS</span></span>

### <span data-ttu-id="63174-133">System.String</span><span class="sxs-lookup"><span data-stu-id="63174-133">System.String</span></span>

## <span data-ttu-id="63174-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="63174-134">OUTPUTS</span></span>

### <span data-ttu-id="63174-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="63174-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="63174-136">Notas</span><span class="sxs-lookup"><span data-stu-id="63174-136">NOTES</span></span>

## <span data-ttu-id="63174-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63174-137">RELATED LINKS</span></span>

[<span data-ttu-id="63174-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="63174-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

