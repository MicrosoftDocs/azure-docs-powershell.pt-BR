---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: aacdcaff98e5cb647c5b4fe1988c24dacc040416
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596075"
---
# <span data-ttu-id="4ebca-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="4ebca-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="4ebca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ebca-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebca-103">Esse cmdlet recupera um número de controle de troca específico por acordo e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="4ebca-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="4ebca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ebca-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ebca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ebca-105">DESCRIPTION</span></span>
<span data-ttu-id="4ebca-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para validar a presença de um número de controle de troca recebido e opcionalmente para remover essa entidade com Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="4ebca-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="4ebca-107">Forneça o parâmetro "-Agreementtype" para especificar se os números de controle X12 ou EDIFACT a serem retornados</span><span class="sxs-lookup"><span data-stu-id="4ebca-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="4ebca-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ebca-108">EXAMPLES</span></span>

### <span data-ttu-id="4ebca-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ebca-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="4ebca-110">Esse comando obtém a conta de integração do X12 de um número de controle de intercâmbio recebido pelo nome do contrato e pelo valor do número do controle.</span><span class="sxs-lookup"><span data-stu-id="4ebca-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="4ebca-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4ebca-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="4ebca-112">Esse comando obtém a conta de integração do EDIFACT de um número de controle de intercâmbio recebido pelo nome do contrato e pelo valor do número do controle.</span><span class="sxs-lookup"><span data-stu-id="4ebca-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="4ebca-113">OS</span><span class="sxs-lookup"><span data-stu-id="4ebca-113">PARAMETERS</span></span>

### <span data-ttu-id="4ebca-114">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="4ebca-114">-AgreementName</span></span>
<span data-ttu-id="4ebca-115">O nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4ebca-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="4ebca-116">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="4ebca-116">-AgreementType</span></span>
<span data-ttu-id="4ebca-117">O tipo de contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4ebca-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="4ebca-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="4ebca-118">-ControlNumberValue</span></span>
<span data-ttu-id="4ebca-119">O valor de número de controle da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4ebca-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="4ebca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebca-120">-DefaultProfile</span></span>
<span data-ttu-id="4ebca-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4ebca-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ebca-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ebca-122">-Name</span></span>
<span data-ttu-id="4ebca-123">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4ebca-123">The integration account name.</span></span>

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

### <span data-ttu-id="4ebca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebca-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ebca-125">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4ebca-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="4ebca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebca-126">CommonParameters</span></span>
<span data-ttu-id="4ebca-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebca-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebca-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ebca-129">INPUTS</span></span>

### <span data-ttu-id="4ebca-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4ebca-130">System.String</span></span>

## <span data-ttu-id="4ebca-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ebca-131">OUTPUTS</span></span>

### <span data-ttu-id="4ebca-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="4ebca-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="4ebca-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ebca-133">NOTES</span></span>

## <span data-ttu-id="4ebca-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ebca-134">RELATED LINKS</span></span>

[<span data-ttu-id="4ebca-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="4ebca-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="4ebca-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="4ebca-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
