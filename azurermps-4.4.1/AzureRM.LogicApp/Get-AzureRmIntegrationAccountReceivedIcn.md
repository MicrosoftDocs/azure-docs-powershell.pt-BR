---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: be42bd7d3e4a6a839182ae36d71f73377460eceb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427889"
---
# <span data-ttu-id="52596-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="52596-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="52596-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52596-102">SYNOPSIS</span></span>
<span data-ttu-id="52596-103">Esse cmdlet recupera um número de controle de troca específico por acordo e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="52596-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52596-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52596-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52596-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52596-105">DESCRIPTION</span></span>
<span data-ttu-id="52596-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para validar a presença de um número de controle de troca recebido e opcionalmente para remover essa entidade com Remove-AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="52596-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="52596-107">Forneça o parâmetro "-Agreementtype" para especificar se os números de controle X12 ou EDIFACT a serem retornados</span><span class="sxs-lookup"><span data-stu-id="52596-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="52596-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52596-108">EXAMPLES</span></span>

### <span data-ttu-id="52596-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52596-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="52596-110">Esse comando obtém a conta de integração do X12 de um número de controle de intercâmbio recebido pelo nome do contrato e pelo valor do número do controle.</span><span class="sxs-lookup"><span data-stu-id="52596-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="52596-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52596-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="52596-112">Esse comando obtém a conta de integração do EDIFACT de um número de controle de intercâmbio recebido pelo nome do contrato e pelo valor do número do controle.</span><span class="sxs-lookup"><span data-stu-id="52596-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="52596-113">OS</span><span class="sxs-lookup"><span data-stu-id="52596-113">PARAMETERS</span></span>

### <span data-ttu-id="52596-114">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="52596-114">-AgreementName</span></span>
<span data-ttu-id="52596-115">O nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="52596-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="52596-116">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="52596-116">-ControlNumberValue</span></span>
<span data-ttu-id="52596-117">O valor de número de controle da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="52596-117">The integration account control number value.</span></span>

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

### <span data-ttu-id="52596-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="52596-118">-Name</span></span>
<span data-ttu-id="52596-119">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="52596-119">The integration account name.</span></span>

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

### <span data-ttu-id="52596-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52596-120">-ResourceGroupName</span></span>
<span data-ttu-id="52596-121">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="52596-121">The integration account resource group name.</span></span>

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

### <span data-ttu-id="52596-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="52596-122">-AgreementType</span></span>
<span data-ttu-id="52596-123">O tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="52596-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="52596-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52596-124">-DefaultProfile</span></span>
<span data-ttu-id="52596-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52596-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52596-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52596-126">CommonParameters</span></span>
<span data-ttu-id="52596-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52596-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52596-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52596-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52596-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52596-129">INPUTS</span></span>

### <span data-ttu-id="52596-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52596-130">System.String</span></span>

## <span data-ttu-id="52596-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52596-131">OUTPUTS</span></span>

### <span data-ttu-id="52596-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="52596-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="52596-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52596-133">NOTES</span></span>

## <span data-ttu-id="52596-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52596-134">RELATED LINKS</span></span>

[<span data-ttu-id="52596-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="52596-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="52596-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="52596-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
