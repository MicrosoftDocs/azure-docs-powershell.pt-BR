---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943021"
---
# <span data-ttu-id="11dad-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="11dad-101">Get-AzDefault</span></span>

## <span data-ttu-id="11dad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11dad-102">SYNOPSIS</span></span>
<span data-ttu-id="11dad-103">Obter os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="11dad-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="11dad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11dad-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11dad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11dad-105">DESCRIPTION</span></span>
<span data-ttu-id="11dad-106">O cmdlet Get-AzDefault Obtém o grupo de recursos que o usuário definiu como padrão no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="11dad-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="11dad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11dad-107">EXAMPLES</span></span>

### <span data-ttu-id="11dad-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11dad-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="11dad-109">Esse comando retorna os padrões atuais se houver padrões definidos ou retorna nada se nenhum padrão for definido.</span><span class="sxs-lookup"><span data-stu-id="11dad-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="11dad-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="11dad-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="11dad-111">Esse comando retorna o grupo de recursos padrão atual se houver um conjunto padrão ou retornará nada se nenhum padrão for definido.</span><span class="sxs-lookup"><span data-stu-id="11dad-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="11dad-112">OS</span><span class="sxs-lookup"><span data-stu-id="11dad-112">PARAMETERS</span></span>

### <span data-ttu-id="11dad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11dad-113">-DefaultProfile</span></span>
<span data-ttu-id="11dad-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11dad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11dad-115">-Resource</span><span class="sxs-lookup"><span data-stu-id="11dad-115">-ResourceGroup</span></span>
<span data-ttu-id="11dad-116">Exibir grupo de recursos padrão</span><span class="sxs-lookup"><span data-stu-id="11dad-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11dad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11dad-117">CommonParameters</span></span>
<span data-ttu-id="11dad-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11dad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11dad-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11dad-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11dad-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11dad-120">INPUTS</span></span>

### <span data-ttu-id="11dad-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="11dad-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="11dad-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11dad-122">OUTPUTS</span></span>

### <span data-ttu-id="11dad-123">Microsoft. Azure. Commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11dad-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="11dad-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11dad-124">NOTES</span></span>

## <span data-ttu-id="11dad-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11dad-125">RELATED LINKS</span></span>
