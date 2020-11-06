---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 2855f5da15de776d7fd85bd267f6a082a85ba5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427897"
---
# <span data-ttu-id="ce467-101">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="ce467-101">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="ce467-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce467-102">SYNOPSIS</span></span>
<span data-ttu-id="ce467-103">Esse cmdlet recupera o valor atual do número de controle de intercâmbio gerado por contrato.</span><span class="sxs-lookup"><span data-stu-id="ce467-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce467-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce467-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce467-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce467-105">DESCRIPTION</span></span>
<span data-ttu-id="ce467-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para recuperar o valor atual do número de controle de intercâmbio gerado para que seja possível gravar novamente um valor aumentado com Set-AzureRmIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="ce467-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzureRmIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="ce467-107">O número do controle do intercâmbio deve ser aumentado para evitar números de controle de intercâmbio duplicados para os números que ainda não puderam ser replicados para a região passiva quando o desastre ocorreu na região ativa.</span><span class="sxs-lookup"><span data-stu-id="ce467-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="ce467-108">Forneça o parâmetro "-Agreementtype" para especificar se os números de controle X12 ou EDIFACT a serem retornados</span><span class="sxs-lookup"><span data-stu-id="ce467-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="ce467-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce467-109">EXAMPLES</span></span>

### <span data-ttu-id="ce467-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce467-110">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="ce467-111">Esse comando obtém a conta de integração gerada X12 o número do controle de intercâmbio por nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="ce467-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="ce467-112">Certifique-se de que o contrato especificado é do tipo "X12"</span><span class="sxs-lookup"><span data-stu-id="ce467-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="ce467-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce467-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="ce467-114">Esse comando obtém a conta de integração gerada EDIFACT o número do controle de intercâmbio por nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="ce467-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="ce467-115">Certifique-se de que o contrato especificado é do tipo "EDIFACT"</span><span class="sxs-lookup"><span data-stu-id="ce467-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="ce467-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce467-116">Example 3</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
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

<span data-ttu-id="ce467-117">Esse comando obtém todos os números de controle de intercâmbio X12 gerados pelo nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ce467-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="ce467-118">OS</span><span class="sxs-lookup"><span data-stu-id="ce467-118">PARAMETERS</span></span>

### <span data-ttu-id="ce467-119">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="ce467-119">-AgreementName</span></span>
<span data-ttu-id="ce467-120">O nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ce467-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="ce467-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce467-121">-Name</span></span>
<span data-ttu-id="ce467-122">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ce467-122">The integration account name.</span></span>

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

### <span data-ttu-id="ce467-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce467-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce467-124">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ce467-124">The integration account resource group name.</span></span>

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

### <span data-ttu-id="ce467-125">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="ce467-125">-AgreementType</span></span>
<span data-ttu-id="ce467-126">O tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ce467-126">The integration account agreement type.</span></span>

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

### <span data-ttu-id="ce467-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce467-127">-DefaultProfile</span></span>
<span data-ttu-id="ce467-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce467-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce467-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce467-129">CommonParameters</span></span>
<span data-ttu-id="ce467-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce467-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce467-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce467-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce467-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce467-132">INPUTS</span></span>

### <span data-ttu-id="ce467-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ce467-133">System.String</span></span>

## <span data-ttu-id="ce467-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce467-134">OUTPUTS</span></span>

### <span data-ttu-id="ce467-135">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="ce467-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="ce467-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce467-136">NOTES</span></span>

## <span data-ttu-id="ce467-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce467-137">RELATED LINKS</span></span>

[<span data-ttu-id="ce467-138">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="ce467-138">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Set-AzureRmIntegrationAccountGeneratedIcn.md)

