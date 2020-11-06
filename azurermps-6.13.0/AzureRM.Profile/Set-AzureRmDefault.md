---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 2836445eabc4b3986a548adf7013ceaa7e75dc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432274"
---
# <span data-ttu-id="a1d23-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="a1d23-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="a1d23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1d23-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d23-103">Define um padrão no contexto atual</span><span class="sxs-lookup"><span data-stu-id="a1d23-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1d23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1d23-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1d23-105">DESCRIPTION</span></span>
<span data-ttu-id="a1d23-106">O cmdlet Set-AzureRmDefault adiciona ou altera os padrões no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="a1d23-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="a1d23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1d23-107">EXAMPLES</span></span>

### <span data-ttu-id="a1d23-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1d23-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="a1d23-109">Este comando define o grupo de recursos padrão para o grupo de recursos especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a1d23-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="a1d23-110">OS</span><span class="sxs-lookup"><span data-stu-id="a1d23-110">PARAMETERS</span></span>

### <span data-ttu-id="a1d23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d23-111">-DefaultProfile</span></span>
<span data-ttu-id="a1d23-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d23-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1d23-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a1d23-113">-Force</span></span>
<span data-ttu-id="a1d23-114">Criar um novo grupo de recursos se o padrão especificado não existir</span><span class="sxs-lookup"><span data-stu-id="a1d23-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="a1d23-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d23-115">-ResourceGroupName</span></span>
<span data-ttu-id="a1d23-116">Nome do grupo de recursos sendo definido como padrão</span><span class="sxs-lookup"><span data-stu-id="a1d23-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d23-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a1d23-117">-Scope</span></span>
<span data-ttu-id="a1d23-118">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="a1d23-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d23-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1d23-119">-Confirm</span></span>
<span data-ttu-id="a1d23-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d23-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d23-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d23-121">-WhatIf</span></span>
<span data-ttu-id="a1d23-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1d23-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d23-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1d23-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d23-124">CommonParameters</span></span>
<span data-ttu-id="a1d23-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d23-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d23-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d23-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1d23-127">INPUTS</span></span>

### <span data-ttu-id="a1d23-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d23-128">System.String</span></span>

## <span data-ttu-id="a1d23-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1d23-129">OUTPUTS</span></span>

### <span data-ttu-id="a1d23-130">Microsoft. Azure. Commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a1d23-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="a1d23-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1d23-131">NOTES</span></span>

## <span data-ttu-id="a1d23-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1d23-132">RELATED LINKS</span></span>
