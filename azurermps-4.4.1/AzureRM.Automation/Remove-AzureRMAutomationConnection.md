---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: aade8dec765a7336292e0350d098417e29d0e360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431820"
---
# <span data-ttu-id="35e45-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="35e45-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="35e45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35e45-102">SYNOPSIS</span></span>
<span data-ttu-id="35e45-103">Remove uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="35e45-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35e45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35e45-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35e45-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35e45-105">DESCRIPTION</span></span>
<span data-ttu-id="35e45-106">O cmdlet **Remove-AzureRmAutomationConnection** remove uma conexão da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="35e45-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="35e45-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35e45-107">EXAMPLES</span></span>

### <span data-ttu-id="35e45-108">Exemplo 1: remover uma conexão</span><span class="sxs-lookup"><span data-stu-id="35e45-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="35e45-109">Esse comando Remove um certificado denominado ContosoConnection na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="35e45-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="35e45-110">OS</span><span class="sxs-lookup"><span data-stu-id="35e45-110">PARAMETERS</span></span>

### <span data-ttu-id="35e45-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35e45-111">-AutomationAccountName</span></span>
<span data-ttu-id="35e45-112">Especifica o nome da conta de automação para a qual esse cmdlet Remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="35e45-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="35e45-113">-Force</span><span class="sxs-lookup"><span data-stu-id="35e45-113">-Force</span></span>
<span data-ttu-id="35e45-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="35e45-114">ps_force</span></span>

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

### <span data-ttu-id="35e45-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="35e45-115">-Name</span></span>
<span data-ttu-id="35e45-116">Especifica o nome da conexão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="35e45-116">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="35e45-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e45-117">-ResourceGroupName</span></span>
<span data-ttu-id="35e45-118">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="35e45-118">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="35e45-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35e45-119">-Confirm</span></span>
<span data-ttu-id="35e45-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e45-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e45-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e45-121">-WhatIf</span></span>
<span data-ttu-id="35e45-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35e45-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e45-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35e45-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e45-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e45-124">-DefaultProfile</span></span>
<span data-ttu-id="35e45-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35e45-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35e45-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e45-126">CommonParameters</span></span>
<span data-ttu-id="35e45-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e45-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e45-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35e45-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e45-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35e45-129">INPUTS</span></span>

## <span data-ttu-id="35e45-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35e45-130">OUTPUTS</span></span>

## <span data-ttu-id="35e45-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35e45-131">NOTES</span></span>

## <span data-ttu-id="35e45-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35e45-132">RELATED LINKS</span></span>

[<span data-ttu-id="35e45-133">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="35e45-133">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="35e45-134">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="35e45-134">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


