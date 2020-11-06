---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d3f5b8a00bed15f7b5fa36fc0bd1a016517eeb89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432476"
---
# <span data-ttu-id="c270a-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c270a-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="c270a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c270a-102">SYNOPSIS</span></span>
<span data-ttu-id="c270a-103">Esse cmdlet recupera um número de controle de troca específico por acordo e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="c270a-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c270a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c270a-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c270a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c270a-105">DESCRIPTION</span></span>
<span data-ttu-id="c270a-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para validar a presença de um número de controle de troca recebido e opcionalmente para remover essa entidade com Remove-AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="c270a-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="c270a-107">Forneça o parâmetro "-Agreementtype" para especificar se os números de controle X12 ou EDIFACT a serem retornados</span><span class="sxs-lookup"><span data-stu-id="c270a-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="c270a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c270a-108">EXAMPLES</span></span>

### <span data-ttu-id="c270a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c270a-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="c270a-110">Esse comando obtém a conta de integração do X12 de um número de controle de intercâmbio recebido pelo nome do contrato e pelo valor do número do controle.</span><span class="sxs-lookup"><span data-stu-id="c270a-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="c270a-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c270a-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="c270a-112">Esse comando obtém a conta de integração do EDIFACT de um número de controle de intercâmbio recebido pelo nome do contrato e pelo valor do número do controle.</span><span class="sxs-lookup"><span data-stu-id="c270a-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="c270a-113">OS</span><span class="sxs-lookup"><span data-stu-id="c270a-113">PARAMETERS</span></span>

### <span data-ttu-id="c270a-114">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="c270a-114">-AgreementName</span></span>
<span data-ttu-id="c270a-115">O nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c270a-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="c270a-116">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="c270a-116">-AgreementType</span></span>
<span data-ttu-id="c270a-117">O tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c270a-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="c270a-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="c270a-118">-ControlNumberValue</span></span>
<span data-ttu-id="c270a-119">O valor de número de controle da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c270a-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="c270a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c270a-120">-DefaultProfile</span></span>
<span data-ttu-id="c270a-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c270a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c270a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c270a-122">-Name</span></span>
<span data-ttu-id="c270a-123">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c270a-123">The integration account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c270a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c270a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c270a-125">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c270a-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="c270a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c270a-126">CommonParameters</span></span>
<span data-ttu-id="c270a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c270a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c270a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c270a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c270a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c270a-129">INPUTS</span></span>

### <span data-ttu-id="c270a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c270a-130">System.String</span></span>

## <span data-ttu-id="c270a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c270a-131">OUTPUTS</span></span>

### <span data-ttu-id="c270a-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="c270a-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="c270a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c270a-133">NOTES</span></span>

## <span data-ttu-id="c270a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c270a-134">RELATED LINKS</span></span>

[<span data-ttu-id="c270a-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c270a-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="c270a-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c270a-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
