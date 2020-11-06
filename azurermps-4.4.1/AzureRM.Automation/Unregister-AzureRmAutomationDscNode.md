---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 76de3ad08e6acb0035cfa2a9ca5d353fcbf38033
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610214"
---
# <span data-ttu-id="ea4c0-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ea4c0-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="ea4c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4c0-103">Remove um nó DSC do gerenciamento por uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea4c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea4c0-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea4c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea4c0-105">DESCRIPTION</span></span>
<span data-ttu-id="ea4c0-106">O cmdlet **Unregister-AzureRmAutomationDscNode** remove um nó de configuração de estado desejado do APS (DSC) da gerência por uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="ea4c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea4c0-107">EXAMPLES</span></span>

### <span data-ttu-id="ea4c0-108">Exemplo 1: remover um nó DSC do Azure do gerenciamento por uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="ea4c0-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="ea4c0-109">Esse comando Remove o nó DSC que tem o GUID especificado do gerenciamento pela conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ea4c0-110">OS</span><span class="sxs-lookup"><span data-stu-id="ea4c0-110">PARAMETERS</span></span>

### <span data-ttu-id="ea4c0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ea4c0-111">-AutomationAccountName</span></span>
<span data-ttu-id="ea4c0-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove um nó DSC.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="ea4c0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ea4c0-113">-Force</span></span>
<span data-ttu-id="ea4c0-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="ea4c0-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4c0-115">-ID</span><span class="sxs-lookup"><span data-stu-id="ea4c0-115">-Id</span></span>
<span data-ttu-id="ea4c0-116">Especifica a ID exclusiva do nó DSC que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-116">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4c0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4c0-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea4c0-118">Especifica o nome de um grupo de recursos em que esse cmdlet cancela o registro de um nó DSC.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-118">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="ea4c0-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea4c0-119">-Confirm</span></span>
<span data-ttu-id="ea4c0-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea4c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea4c0-121">-WhatIf</span></span>
<span data-ttu-id="ea4c0-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea4c0-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea4c0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4c0-124">-DefaultProfile</span></span>
<span data-ttu-id="ea4c0-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea4c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4c0-126">CommonParameters</span></span>
<span data-ttu-id="ea4c0-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea4c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4c0-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4c0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4c0-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea4c0-129">INPUTS</span></span>

## <span data-ttu-id="ea4c0-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea4c0-130">OUTPUTS</span></span>

### <span data-ttu-id="ea4c0-131">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="ea4c0-131">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="ea4c0-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea4c0-132">NOTES</span></span>

## <span data-ttu-id="ea4c0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea4c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="ea4c0-134">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ea4c0-134">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="ea4c0-135">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ea4c0-135">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="ea4c0-136">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ea4c0-136">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


