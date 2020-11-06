---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: 9598280ecae0ce8aca94fd16ae40928dba7a2404
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428625"
---
# <span data-ttu-id="14c8d-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="14c8d-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="14c8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="14c8d-103">Remove um tipo de conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="14c8d-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14c8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14c8d-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14c8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="14c8d-106">O cmdlet **Remove-AzureRmAutomationConnectionType** remove um tipo de conexão da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="14c8d-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="14c8d-107">Todas as conexões associadas ao tipo de conexão que você exclui se tornam inutilizáveis.</span><span class="sxs-lookup"><span data-stu-id="14c8d-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="14c8d-108">Remova-os, a menos que você crie um novo tipo de conexão que atenda aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="14c8d-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="14c8d-109">O tipo tem o mesmo nome que o tipo de conexão original.</span><span class="sxs-lookup"><span data-stu-id="14c8d-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="14c8d-110">O tipo tem as mesmas definições de campo que o tipo de conexão original.</span><span class="sxs-lookup"><span data-stu-id="14c8d-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="14c8d-111">Ele pode ter campos adicionais.</span><span class="sxs-lookup"><span data-stu-id="14c8d-111">It can have additional fields.</span></span>

## <span data-ttu-id="14c8d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14c8d-112">EXAMPLES</span></span>

### <span data-ttu-id="14c8d-113">Exemplo 1: remover um tipo de conexão</span><span class="sxs-lookup"><span data-stu-id="14c8d-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="14c8d-114">Esse comando Remove um tipo de conexão chamado ContosoConnectionType na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="14c8d-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="14c8d-115">OS</span><span class="sxs-lookup"><span data-stu-id="14c8d-115">PARAMETERS</span></span>

### <span data-ttu-id="14c8d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="14c8d-116">-AutomationAccountName</span></span>
<span data-ttu-id="14c8d-117">Especifica o nome da conta de automação para a qual esse cmdlet Remove um tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="14c8d-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="14c8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c8d-118">-DefaultProfile</span></span>
<span data-ttu-id="14c8d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="14c8d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14c8d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="14c8d-120">-Force</span></span>
<span data-ttu-id="14c8d-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="14c8d-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c8d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="14c8d-122">-Name</span></span>
<span data-ttu-id="14c8d-123">Especifica o nome do tipo de conexão de automação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="14c8d-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="14c8d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c8d-124">-ResourceGroupName</span></span>
<span data-ttu-id="14c8d-125">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um tipo de conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="14c8d-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="14c8d-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14c8d-126">-Confirm</span></span>
<span data-ttu-id="14c8d-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14c8d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14c8d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14c8d-128">-WhatIf</span></span>
<span data-ttu-id="14c8d-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14c8d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14c8d-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14c8d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14c8d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c8d-131">CommonParameters</span></span>
<span data-ttu-id="14c8d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c8d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c8d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c8d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c8d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14c8d-134">INPUTS</span></span>

### <span data-ttu-id="14c8d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="14c8d-135">System.String</span></span>

## <span data-ttu-id="14c8d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14c8d-136">OUTPUTS</span></span>

### <span data-ttu-id="14c8d-137">System. void</span><span class="sxs-lookup"><span data-stu-id="14c8d-137">System.Void</span></span>

## <span data-ttu-id="14c8d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14c8d-138">NOTES</span></span>

## <span data-ttu-id="14c8d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14c8d-139">RELATED LINKS</span></span>

[<span data-ttu-id="14c8d-140">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="14c8d-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


