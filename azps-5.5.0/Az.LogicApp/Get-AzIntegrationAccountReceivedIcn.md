---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113623"
---
# <span data-ttu-id="41e0b-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="41e0b-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="41e0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="41e0b-103">Este cmdlet recupera um número de controle de troca de troca recebido específico por contrato e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="41e0b-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="41e0b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41e0b-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41e0b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="41e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="41e0b-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para validar a presença de um número de controle de troca recebido e, opcionalmente, remover essa entidade com Remove-AzIntegrationAccountRecountIcn.</span><span class="sxs-lookup"><span data-stu-id="41e0b-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="41e0b-107">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem ser retornados</span><span class="sxs-lookup"><span data-stu-id="41e0b-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="41e0b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41e0b-108">EXAMPLES</span></span>

### <span data-ttu-id="41e0b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41e0b-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="41e0b-110">Esse comando obtém a conta de integração X12 recebida pelo número do controle de troca por nome de contrato e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="41e0b-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="41e0b-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="41e0b-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="41e0b-112">Esse comando obtém a conta de integração Edifact recebida número do controle de troca por nome de contrato e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="41e0b-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="41e0b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41e0b-113">PARAMETERS</span></span>

### <span data-ttu-id="41e0b-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="41e0b-114">-AgreementName</span></span>
<span data-ttu-id="41e0b-115">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="41e0b-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="41e0b-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="41e0b-116">-AgreementType</span></span>
<span data-ttu-id="41e0b-117">O tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="41e0b-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="41e0b-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="41e0b-118">-ControlNumberValue</span></span>
<span data-ttu-id="41e0b-119">O valor de número do controle de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="41e0b-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="41e0b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e0b-120">-DefaultProfile</span></span>
<span data-ttu-id="41e0b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="41e0b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41e0b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="41e0b-122">-Name</span></span>
<span data-ttu-id="41e0b-123">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="41e0b-123">The integration account name.</span></span>

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

### <span data-ttu-id="41e0b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e0b-124">-ResourceGroupName</span></span>
<span data-ttu-id="41e0b-125">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="41e0b-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="41e0b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e0b-126">CommonParameters</span></span>
<span data-ttu-id="41e0b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e0b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e0b-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41e0b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e0b-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="41e0b-129">INPUTS</span></span>

### <span data-ttu-id="41e0b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="41e0b-130">System.String</span></span>

## <span data-ttu-id="41e0b-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="41e0b-131">OUTPUTS</span></span>

### <span data-ttu-id="41e0b-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="41e0b-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="41e0b-133">Notas</span><span class="sxs-lookup"><span data-stu-id="41e0b-133">NOTES</span></span>

## <span data-ttu-id="41e0b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41e0b-134">RELATED LINKS</span></span>

[<span data-ttu-id="41e0b-135">Set-AzIntegrationAccountRecountIcn</span><span class="sxs-lookup"><span data-stu-id="41e0b-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="41e0b-136">Remove-AzIntegrationAccountRecountIcn</span><span class="sxs-lookup"><span data-stu-id="41e0b-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
