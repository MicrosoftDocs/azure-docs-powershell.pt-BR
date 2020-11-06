---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: a0699722a4275855fc2203ac4a38ee5ebdee58f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597537"
---
# <span data-ttu-id="8b981-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b981-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="8b981-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b981-102">SYNOPSIS</span></span>
<span data-ttu-id="8b981-103">Exclui uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="8b981-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="8b981-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b981-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b981-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b981-105">DESCRIPTION</span></span>
<span data-ttu-id="8b981-106">O cmdlet **Remove-AzCognitiveServicesAccount** exclui a conta de serviços cognitivas especificada.</span><span class="sxs-lookup"><span data-stu-id="8b981-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="8b981-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b981-107">EXAMPLES</span></span>

### <span data-ttu-id="8b981-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8b981-108">Example 1</span></span>
<span data-ttu-id="8b981-109">Esse comando não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="8b981-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="8b981-110">OS</span><span class="sxs-lookup"><span data-stu-id="8b981-110">PARAMETERS</span></span>

### <span data-ttu-id="8b981-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b981-111">-DefaultProfile</span></span>
<span data-ttu-id="8b981-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8b981-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b981-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8b981-113">-Force</span></span>
<span data-ttu-id="8b981-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b981-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b981-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b981-115">-Name</span></span>
<span data-ttu-id="8b981-116">Especifica o nome da conta a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="8b981-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="8b981-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b981-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b981-118">Especifica o nome do grupo de recursos ao qual a conta de serviços cognitiva está atribuída.</span><span class="sxs-lookup"><span data-stu-id="8b981-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="8b981-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b981-119">-Confirm</span></span>
<span data-ttu-id="8b981-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b981-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b981-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b981-121">-WhatIf</span></span>
<span data-ttu-id="8b981-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b981-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b981-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b981-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b981-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b981-124">CommonParameters</span></span>
<span data-ttu-id="8b981-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b981-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b981-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b981-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b981-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b981-127">INPUTS</span></span>

### <span data-ttu-id="8b981-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8b981-128">System.String</span></span>

## <span data-ttu-id="8b981-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b981-129">OUTPUTS</span></span>

### <span data-ttu-id="8b981-130">System. void</span><span class="sxs-lookup"><span data-stu-id="8b981-130">System.Void</span></span>

## <span data-ttu-id="8b981-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b981-131">NOTES</span></span>

## <span data-ttu-id="8b981-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b981-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b981-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b981-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8b981-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b981-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8b981-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b981-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


