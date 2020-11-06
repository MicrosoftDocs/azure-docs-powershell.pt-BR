---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 2c8496af209cc72ebb6cb9a2ed40ae6033ce7268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440092"
---
# <span data-ttu-id="939fa-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="939fa-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="939fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="939fa-102">SYNOPSIS</span></span>
<span data-ttu-id="939fa-103">Exclui uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="939fa-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="939fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="939fa-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="939fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="939fa-105">DESCRIPTION</span></span>
<span data-ttu-id="939fa-106">O cmdlet **Remove-AzureRmCognitiveServicesAccount** exclui a conta de serviços cognitivas especificada.</span><span class="sxs-lookup"><span data-stu-id="939fa-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="939fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="939fa-107">EXAMPLES</span></span>

### <span data-ttu-id="939fa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="939fa-108">Example 1</span></span>
<span data-ttu-id="939fa-109">Esse comando não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="939fa-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="939fa-110">OS</span><span class="sxs-lookup"><span data-stu-id="939fa-110">PARAMETERS</span></span>

### <span data-ttu-id="939fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="939fa-111">-DefaultProfile</span></span>
<span data-ttu-id="939fa-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="939fa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="939fa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="939fa-113">-Force</span></span>
<span data-ttu-id="939fa-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="939fa-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="939fa-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="939fa-115">-Name</span></span>
<span data-ttu-id="939fa-116">Especifica o nome da conta a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="939fa-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="939fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="939fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="939fa-118">Especifica o nome do grupo de recursos ao qual a conta de serviços cognitiva está atribuída.</span><span class="sxs-lookup"><span data-stu-id="939fa-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="939fa-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="939fa-119">-Confirm</span></span>
<span data-ttu-id="939fa-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="939fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="939fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="939fa-121">-WhatIf</span></span>
<span data-ttu-id="939fa-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="939fa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="939fa-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="939fa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="939fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="939fa-124">CommonParameters</span></span>
<span data-ttu-id="939fa-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="939fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="939fa-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="939fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="939fa-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="939fa-127">INPUTS</span></span>

### <span data-ttu-id="939fa-128">System. String</span><span class="sxs-lookup"><span data-stu-id="939fa-128">System.String</span></span>

## <span data-ttu-id="939fa-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="939fa-129">OUTPUTS</span></span>

### <span data-ttu-id="939fa-130">System. void</span><span class="sxs-lookup"><span data-stu-id="939fa-130">System.Void</span></span>

## <span data-ttu-id="939fa-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="939fa-131">NOTES</span></span>

## <span data-ttu-id="939fa-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="939fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="939fa-133">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="939fa-133">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="939fa-134">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="939fa-134">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="939fa-135">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="939fa-135">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


