---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 20d66412002e8feb1b4007608091cdbf0422b6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439851"
---
# <span data-ttu-id="02854-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="02854-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="02854-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02854-102">SYNOPSIS</span></span>
<span data-ttu-id="02854-103">Obter os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="02854-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02854-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02854-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02854-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02854-105">DESCRIPTION</span></span>
<span data-ttu-id="02854-106">O cmdlet Get-AzureRmDefault Obtém o grupo de recursos que o usuário definiu como padrão no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="02854-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="02854-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02854-107">EXAMPLES</span></span>

### <span data-ttu-id="02854-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02854-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="02854-109">Esse comando retorna os padrões atuais se houver padrões definidos ou retorna nada se nenhum padrão for definido.</span><span class="sxs-lookup"><span data-stu-id="02854-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="02854-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="02854-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="02854-111">Esse comando retorna o grupo de recursos padrão atual se houver um conjunto padrão ou retornará nada se nenhum padrão for definido.</span><span class="sxs-lookup"><span data-stu-id="02854-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="02854-112">OS</span><span class="sxs-lookup"><span data-stu-id="02854-112">PARAMETERS</span></span>

### <span data-ttu-id="02854-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02854-113">-DefaultProfile</span></span>
<span data-ttu-id="02854-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02854-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02854-115">-Resource</span><span class="sxs-lookup"><span data-stu-id="02854-115">-ResourceGroup</span></span>
<span data-ttu-id="02854-116">Exibir grupo de recursos padrão</span><span class="sxs-lookup"><span data-stu-id="02854-116">Display Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02854-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02854-117">CommonParameters</span></span>
<span data-ttu-id="02854-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02854-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02854-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02854-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02854-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02854-120">INPUTS</span></span>

### <span data-ttu-id="02854-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="02854-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="02854-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02854-122">OUTPUTS</span></span>

### <span data-ttu-id="02854-123">Microsoft. Azure. Management. Internal. Resources. Models. resourcement</span><span class="sxs-lookup"><span data-stu-id="02854-123">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="02854-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02854-124">NOTES</span></span>

## <span data-ttu-id="02854-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02854-125">RELATED LINKS</span></span>

