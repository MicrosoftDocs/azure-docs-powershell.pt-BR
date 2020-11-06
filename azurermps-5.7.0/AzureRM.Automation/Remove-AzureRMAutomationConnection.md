---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 4fb4bbab5c774cacd274754a106aacfeebdb533c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440880"
---
# <span data-ttu-id="5e5c9-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5e5c9-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="5e5c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5c9-103">Remove uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e5c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e5c9-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e5c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="5e5c9-106">O cmdlet **Remove-AzureRmAutomationConnection** remove uma conexão da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="5e5c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e5c9-107">EXAMPLES</span></span>

### <span data-ttu-id="5e5c9-108">Exemplo 1: remover uma conexão</span><span class="sxs-lookup"><span data-stu-id="5e5c9-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5e5c9-109">Esse comando Remove um certificado denominado ContosoConnection na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5e5c9-110">OS</span><span class="sxs-lookup"><span data-stu-id="5e5c9-110">PARAMETERS</span></span>

### <span data-ttu-id="5e5c9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5e5c9-111">-AutomationAccountName</span></span>
<span data-ttu-id="5e5c9-112">Especifica o nome da conta de automação para a qual esse cmdlet Remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="5e5c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e5c9-113">-DefaultProfile</span></span>
<span data-ttu-id="5e5c9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5e5c9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e5c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5e5c9-115">-Force</span></span>
<span data-ttu-id="5e5c9-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="5e5c9-116">ps_force</span></span>

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

### <span data-ttu-id="5e5c9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e5c9-117">-Name</span></span>
<span data-ttu-id="5e5c9-118">Especifica o nome da conexão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e5c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e5c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e5c9-120">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="5e5c9-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e5c9-121">-Confirm</span></span>
<span data-ttu-id="5e5c9-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e5c9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e5c9-123">-WhatIf</span></span>
<span data-ttu-id="5e5c9-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e5c9-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e5c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5c9-126">CommonParameters</span></span>
<span data-ttu-id="5e5c9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5c9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e5c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5c9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e5c9-129">INPUTS</span></span>

### <span data-ttu-id="5e5c9-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5e5c9-130">None</span></span>
<span data-ttu-id="5e5c9-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5e5c9-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e5c9-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e5c9-132">OUTPUTS</span></span>

## <span data-ttu-id="5e5c9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e5c9-133">NOTES</span></span>

## <span data-ttu-id="5e5c9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e5c9-134">RELATED LINKS</span></span>

[<span data-ttu-id="5e5c9-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5e5c9-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="5e5c9-136">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5e5c9-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

