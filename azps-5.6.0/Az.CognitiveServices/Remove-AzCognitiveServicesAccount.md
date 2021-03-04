---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: f35aee632f4f5c5ee2be36ac3eea92c5ec5f59f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890646"
---
# <span data-ttu-id="7ed95-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ed95-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="7ed95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ed95-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed95-103">Exclui uma conta dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="7ed95-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="7ed95-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ed95-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ed95-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ed95-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed95-106">O cmdlet **Remove-AzCognitiveServicesAccount** exclui a conta especificada dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="7ed95-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="7ed95-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ed95-107">EXAMPLES</span></span>

### <span data-ttu-id="7ed95-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ed95-108">Example 1</span></span>
<span data-ttu-id="7ed95-109">Este comando não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="7ed95-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="7ed95-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ed95-110">PARAMETERS</span></span>

### <span data-ttu-id="7ed95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed95-111">-DefaultProfile</span></span>
<span data-ttu-id="7ed95-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7ed95-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ed95-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7ed95-113">-Force</span></span>
<span data-ttu-id="7ed95-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7ed95-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ed95-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7ed95-115">-Name</span></span>
<span data-ttu-id="7ed95-116">Especifica o nome da conta a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7ed95-116">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed95-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ed95-118">Especifica o nome do grupo de recursos ao quais a conta dos Serviços Cognitivos é atribuída.</span><span class="sxs-lookup"><span data-stu-id="7ed95-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="7ed95-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ed95-119">-Confirm</span></span>
<span data-ttu-id="7ed95-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed95-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed95-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed95-121">-WhatIf</span></span>
<span data-ttu-id="7ed95-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ed95-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed95-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ed95-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed95-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed95-124">CommonParameters</span></span>
<span data-ttu-id="7ed95-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed95-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed95-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ed95-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed95-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ed95-127">INPUTS</span></span>

### <span data-ttu-id="7ed95-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7ed95-128">System.String</span></span>

## <span data-ttu-id="7ed95-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ed95-129">OUTPUTS</span></span>

### <span data-ttu-id="7ed95-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="7ed95-130">System.Void</span></span>

## <span data-ttu-id="7ed95-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ed95-131">NOTES</span></span>

## <span data-ttu-id="7ed95-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ed95-132">RELATED LINKS</span></span>

[<span data-ttu-id="7ed95-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ed95-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7ed95-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ed95-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7ed95-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ed95-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


