---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: df7266548b616615fa45131c21f40622894ffe9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886458"
---
# <span data-ttu-id="082b8-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="082b8-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="082b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="082b8-102">SYNOPSIS</span></span>
<span data-ttu-id="082b8-103">Este cmdlet recupera um número de controle de intercâmbio recebido específico por contrato e valor de número de controle.</span><span class="sxs-lookup"><span data-stu-id="082b8-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="082b8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="082b8-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="082b8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="082b8-105">DESCRIPTION</span></span>
<span data-ttu-id="082b8-106">Esse cmdlet deve ser usado em cenários de recuperação de desastres para validar a presença de um número de controle de intercâmbio recebido e, opcionalmente, remover essa entidade com Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="082b8-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="082b8-107">Forneça o parâmetro "-AgreementType" para especificar se os números de controle X12 ou Edifact devem retornar</span><span class="sxs-lookup"><span data-stu-id="082b8-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="082b8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="082b8-108">EXAMPLES</span></span>

### <span data-ttu-id="082b8-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="082b8-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="082b8-110">Este comando obtém a conta de integração X12 recebida número de controle de intercâmbio pelo nome do contrato e o valor do número de controle.</span><span class="sxs-lookup"><span data-stu-id="082b8-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="082b8-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="082b8-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="082b8-112">Este comando obtém a conta de integração Edifact recebida número de controle de intercâmbio pelo nome do contrato e o valor do número de controle.</span><span class="sxs-lookup"><span data-stu-id="082b8-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="082b8-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="082b8-113">PARAMETERS</span></span>

### <span data-ttu-id="082b8-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="082b8-114">-AgreementName</span></span>
<span data-ttu-id="082b8-115">O nome do contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="082b8-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="082b8-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="082b8-116">-AgreementType</span></span>
<span data-ttu-id="082b8-117">O tipo de contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="082b8-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="082b8-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="082b8-118">-ControlNumberValue</span></span>
<span data-ttu-id="082b8-119">O valor do número de controle da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="082b8-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="082b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082b8-120">-DefaultProfile</span></span>
<span data-ttu-id="082b8-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="082b8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="082b8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="082b8-122">-Name</span></span>
<span data-ttu-id="082b8-123">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="082b8-123">The integration account name.</span></span>

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

### <span data-ttu-id="082b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="082b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="082b8-125">O nome do grupo de recursos da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="082b8-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="082b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082b8-126">CommonParameters</span></span>
<span data-ttu-id="082b8-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="082b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082b8-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="082b8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082b8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="082b8-129">INPUTS</span></span>

### <span data-ttu-id="082b8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="082b8-130">System.String</span></span>

## <span data-ttu-id="082b8-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="082b8-131">OUTPUTS</span></span>

### <span data-ttu-id="082b8-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="082b8-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="082b8-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="082b8-133">NOTES</span></span>

## <span data-ttu-id="082b8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="082b8-134">RELATED LINKS</span></span>

[<span data-ttu-id="082b8-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="082b8-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="082b8-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="082b8-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
