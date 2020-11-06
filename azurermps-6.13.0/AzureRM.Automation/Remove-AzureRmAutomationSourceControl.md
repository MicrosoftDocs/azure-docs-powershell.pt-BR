---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSourceControl.md
ms.openlocfilehash: abd09a195db5652d2dfdffce17096116895eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428613"
---
# <span data-ttu-id="ded14-101">Remove-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="ded14-101">Remove-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="ded14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ded14-102">SYNOPSIS</span></span>
<span data-ttu-id="ded14-103">Remove um controle de origem da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ded14-103">Removes an Azure Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ded14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ded14-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ded14-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ded14-105">DESCRIPTION</span></span>
<span data-ttu-id="ded14-106">O cmdlet Remove-AzureRmAutomationSourceControl remove um controle de origem da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ded14-106">The Remove-AzureRmAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="ded14-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ded14-107">EXAMPLES</span></span>

### <span data-ttu-id="ded14-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ded14-108">Example 1</span></span>
<span data-ttu-id="ded14-109">Esse comando Remove o controle de origem de automação chamado VSTSNative na conta chamada devAccount.</span><span class="sxs-lookup"><span data-stu-id="ded14-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="ded14-110">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="ded14-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="ded14-111">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="ded14-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="ded14-112">OS</span><span class="sxs-lookup"><span data-stu-id="ded14-112">PARAMETERS</span></span>

### <span data-ttu-id="ded14-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ded14-113">-AutomationAccountName</span></span>
<span data-ttu-id="ded14-114">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ded14-114">The automation account name.</span></span>

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

### <span data-ttu-id="ded14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded14-115">-DefaultProfile</span></span>
<span data-ttu-id="ded14-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ded14-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ded14-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ded14-117">-Name</span></span>
<span data-ttu-id="ded14-118">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="ded14-118">The source control name.</span></span>

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

### <span data-ttu-id="ded14-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ded14-119">-PassThru</span></span>
<span data-ttu-id="ded14-120">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ded14-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ded14-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ded14-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ded14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded14-122">-ResourceGroupName</span></span>
<span data-ttu-id="ded14-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ded14-123">The resource group name.</span></span>

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

### <span data-ttu-id="ded14-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ded14-124">-Confirm</span></span>
<span data-ttu-id="ded14-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ded14-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ded14-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ded14-126">-WhatIf</span></span>
<span data-ttu-id="ded14-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ded14-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ded14-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ded14-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ded14-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded14-129">CommonParameters</span></span>
<span data-ttu-id="ded14-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded14-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded14-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded14-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded14-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ded14-132">INPUTS</span></span>

### <span data-ttu-id="ded14-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ded14-133">System.String</span></span>

## <span data-ttu-id="ded14-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ded14-134">OUTPUTS</span></span>

### <span data-ttu-id="ded14-135">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="ded14-135">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="ded14-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ded14-136">NOTES</span></span>

## <span data-ttu-id="ded14-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ded14-137">RELATED LINKS</span></span>
