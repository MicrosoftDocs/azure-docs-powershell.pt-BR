---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117891"
---
# <span data-ttu-id="0f58d-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f58d-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="0f58d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f58d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f58d-103">Exclui uma conta dos Serviços Cognitivas.</span><span class="sxs-lookup"><span data-stu-id="0f58d-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="0f58d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f58d-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f58d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f58d-105">DESCRIPTION</span></span>
<span data-ttu-id="0f58d-106">O **cmdlet Remove-AzCognitiveServicesAccount** exclui a conta especificada dos Serviços Cognitivas.</span><span class="sxs-lookup"><span data-stu-id="0f58d-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="0f58d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0f58d-107">EXAMPLES</span></span>

### <span data-ttu-id="0f58d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f58d-108">Example 1</span></span>
<span data-ttu-id="0f58d-109">Este comando não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="0f58d-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="0f58d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f58d-110">PARAMETERS</span></span>

### <span data-ttu-id="0f58d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f58d-111">-DefaultProfile</span></span>
<span data-ttu-id="0f58d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0f58d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f58d-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0f58d-113">-Force</span></span>
<span data-ttu-id="0f58d-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0f58d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f58d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f58d-115">-Name</span></span>
<span data-ttu-id="0f58d-116">Especifica o nome da conta a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="0f58d-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="0f58d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f58d-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f58d-118">Especifica o nome do grupo de recursos ao quais a conta dos Serviços Cognitivas está atribuída.</span><span class="sxs-lookup"><span data-stu-id="0f58d-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="0f58d-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0f58d-119">-Confirm</span></span>
<span data-ttu-id="0f58d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f58d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f58d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f58d-121">-WhatIf</span></span>
<span data-ttu-id="0f58d-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0f58d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f58d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f58d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f58d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f58d-124">CommonParameters</span></span>
<span data-ttu-id="0f58d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f58d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f58d-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f58d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f58d-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="0f58d-127">INPUTS</span></span>

### <span data-ttu-id="0f58d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0f58d-128">System.String</span></span>

## <span data-ttu-id="0f58d-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="0f58d-129">OUTPUTS</span></span>

### <span data-ttu-id="0f58d-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="0f58d-130">System.Void</span></span>

## <span data-ttu-id="0f58d-131">Notas</span><span class="sxs-lookup"><span data-stu-id="0f58d-131">NOTES</span></span>

## <span data-ttu-id="0f58d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f58d-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f58d-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f58d-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0f58d-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f58d-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0f58d-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0f58d-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


