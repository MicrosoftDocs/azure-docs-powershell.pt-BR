---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: c76475a36536e6da68bc7ec5a39790ee96409ea3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426820"
---
# <span data-ttu-id="66d30-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="66d30-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="66d30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66d30-102">SYNOPSIS</span></span>
<span data-ttu-id="66d30-103">Remove um tipo de conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="66d30-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66d30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66d30-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66d30-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66d30-105">DESCRIPTION</span></span>
<span data-ttu-id="66d30-106">O cmdlet **Remove-AzureRmAutomationConnectionType** remove um tipo de conexão da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="66d30-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>

<span data-ttu-id="66d30-107">Todas as conexões associadas ao tipo de conexão que você exclui se tornam inutilizáveis.</span><span class="sxs-lookup"><span data-stu-id="66d30-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="66d30-108">Remova-os, a menos que você crie um novo tipo de conexão que atenda aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="66d30-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 

- <span data-ttu-id="66d30-109">O tipo tem o mesmo nome que o tipo de conexão original.</span><span class="sxs-lookup"><span data-stu-id="66d30-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="66d30-110">O tipo tem as mesmas definições de campo que o tipo de conexão original.</span><span class="sxs-lookup"><span data-stu-id="66d30-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="66d30-111">Ele pode ter campos adicionais.</span><span class="sxs-lookup"><span data-stu-id="66d30-111">It can have additional fields.</span></span>

## <span data-ttu-id="66d30-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66d30-112">EXAMPLES</span></span>

### <span data-ttu-id="66d30-113">Exemplo 1: remover um tipo de conexão</span><span class="sxs-lookup"><span data-stu-id="66d30-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="66d30-114">Esse comando Remove um tipo de conexão chamado ContosoConnectionType na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="66d30-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="66d30-115">OS</span><span class="sxs-lookup"><span data-stu-id="66d30-115">PARAMETERS</span></span>

### <span data-ttu-id="66d30-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="66d30-116">-AutomationAccountName</span></span>
<span data-ttu-id="66d30-117">Especifica o nome da conta de automação para a qual esse cmdlet Remove um tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="66d30-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d30-118">-DefaultProfile</span></span>
<span data-ttu-id="66d30-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="66d30-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66d30-120">-Force</span><span class="sxs-lookup"><span data-stu-id="66d30-120">-Force</span></span>
<span data-ttu-id="66d30-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="66d30-121">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66d30-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="66d30-122">-Name</span></span>
<span data-ttu-id="66d30-123">Especifica o nome do tipo de conexão de automação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="66d30-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d30-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66d30-124">-ResourceGroupName</span></span>
<span data-ttu-id="66d30-125">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um tipo de conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="66d30-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d30-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66d30-126">-Confirm</span></span>
<span data-ttu-id="66d30-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66d30-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66d30-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66d30-128">-WhatIf</span></span>
<span data-ttu-id="66d30-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66d30-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66d30-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66d30-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66d30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d30-131">CommonParameters</span></span>
<span data-ttu-id="66d30-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d30-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d30-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d30-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66d30-134">INPUTS</span></span>

### <span data-ttu-id="66d30-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="66d30-135">None</span></span>
<span data-ttu-id="66d30-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="66d30-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66d30-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66d30-137">OUTPUTS</span></span>

## <span data-ttu-id="66d30-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66d30-138">NOTES</span></span>

## <span data-ttu-id="66d30-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66d30-139">RELATED LINKS</span></span>

[<span data-ttu-id="66d30-140">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="66d30-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


