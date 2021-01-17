---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430579"
---
# <span data-ttu-id="9a00c-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="9a00c-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="9a00c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a00c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a00c-103">Modifica o valor de um campo em uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="9a00c-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="9a00c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a00c-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a00c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a00c-105">DESCRIPTION</span></span>
<span data-ttu-id="9a00c-106">O cmdlet **set-AzAutomationConnectionFieldValue** modifica o valor de um campo em uma conexão na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9a00c-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="9a00c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a00c-107">EXAMPLES</span></span>

### <span data-ttu-id="9a00c-108">Exemplo 1: alterar um valor de campo em uma conexão</span><span class="sxs-lookup"><span data-stu-id="9a00c-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9a00c-109">Esse comando altera a ID da assinatura para a conexão do Azure chamada ContosoConnection na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="9a00c-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="9a00c-110">OS</span><span class="sxs-lookup"><span data-stu-id="9a00c-110">PARAMETERS</span></span>

### <span data-ttu-id="9a00c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a00c-111">-AutomationAccountName</span></span>
<span data-ttu-id="9a00c-112">Especifica o nome da conta de automação para a qual esse cmdlet modifica um campo em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="9a00c-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a00c-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="9a00c-113">-ConnectionFieldName</span></span>
<span data-ttu-id="9a00c-114">Especifica um nome para o campo que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9a00c-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9a00c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a00c-115">-DefaultProfile</span></span>
<span data-ttu-id="9a00c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9a00c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a00c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a00c-117">-Name</span></span>
<span data-ttu-id="9a00c-118">Especifica um nome para a conexão para a qual esse cmdlet modifica um campo.</span><span class="sxs-lookup"><span data-stu-id="9a00c-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a00c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a00c-119">-ResourceGroupName</span></span>
<span data-ttu-id="9a00c-120">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um campo em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="9a00c-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a00c-121">-Valor</span><span class="sxs-lookup"><span data-stu-id="9a00c-121">-Value</span></span>
<span data-ttu-id="9a00c-122">Especifica um valor a ser modificado no campo de conexão.</span><span class="sxs-lookup"><span data-stu-id="9a00c-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a00c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a00c-123">CommonParameters</span></span>
<span data-ttu-id="9a00c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a00c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a00c-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a00c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a00c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a00c-126">INPUTS</span></span>

### <span data-ttu-id="9a00c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9a00c-127">System.String</span></span>

### <span data-ttu-id="9a00c-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="9a00c-128">System.Object</span></span>

## <span data-ttu-id="9a00c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a00c-129">OUTPUTS</span></span>

### <span data-ttu-id="9a00c-130">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="9a00c-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9a00c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a00c-131">NOTES</span></span>

## <span data-ttu-id="9a00c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a00c-132">RELATED LINKS</span></span>

[<span data-ttu-id="9a00c-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9a00c-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


