---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114780"
---
# <span data-ttu-id="96cfa-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="96cfa-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="96cfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="96cfa-103">Obtém a conta.</span><span class="sxs-lookup"><span data-stu-id="96cfa-103">Gets the account.</span></span>

## <span data-ttu-id="96cfa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96cfa-104">SYNTAX</span></span>

### <span data-ttu-id="96cfa-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96cfa-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96cfa-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96cfa-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96cfa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96cfa-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96cfa-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="96cfa-108">DESCRIPTION</span></span>
<span data-ttu-id="96cfa-109">O Get-AzMapsAccount cmdlet obtém uma conta provisionada do Azure Maps, seja por grupo de recursos e nome, ou por ID do recurso. Além disso, ele pode retornar uma lista de todas as contas no ResourceGroup ou todas as contas do Azure Maps para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="96cfa-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="96cfa-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96cfa-110">EXAMPLES</span></span>

### <span data-ttu-id="96cfa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96cfa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="96cfa-112">Obtém a conta chamada MyAccount no grupo de recursos MyResourceGroup, se ela existir.</span><span class="sxs-lookup"><span data-stu-id="96cfa-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="96cfa-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="96cfa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="96cfa-114">Obtém todas as contas do Azure Maps no grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="96cfa-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="96cfa-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="96cfa-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="96cfa-116">Obtém todas as contas do Azure Maps na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="96cfa-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="96cfa-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="96cfa-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="96cfa-118">Obtém a conta Mapas especificada pela ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="96cfa-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="96cfa-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96cfa-119">PARAMETERS</span></span>

### <span data-ttu-id="96cfa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cfa-120">-DefaultProfile</span></span>
<span data-ttu-id="96cfa-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96cfa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96cfa-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="96cfa-122">-Name</span></span>
<span data-ttu-id="96cfa-123">Nome da Conta do Mapas.</span><span class="sxs-lookup"><span data-stu-id="96cfa-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96cfa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96cfa-124">-ResourceGroupName</span></span>
<span data-ttu-id="96cfa-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96cfa-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96cfa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96cfa-126">-ResourceId</span></span>
<span data-ttu-id="96cfa-127">Mapeia o ResourceId da Conta.</span><span class="sxs-lookup"><span data-stu-id="96cfa-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96cfa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cfa-128">CommonParameters</span></span>
<span data-ttu-id="96cfa-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96cfa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cfa-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cfa-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cfa-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="96cfa-131">INPUTS</span></span>

### <span data-ttu-id="96cfa-132">System.String</span><span class="sxs-lookup"><span data-stu-id="96cfa-132">System.String</span></span>

## <span data-ttu-id="96cfa-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="96cfa-133">OUTPUTS</span></span>

### <span data-ttu-id="96cfa-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="96cfa-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="96cfa-135">Notas</span><span class="sxs-lookup"><span data-stu-id="96cfa-135">NOTES</span></span>

## <span data-ttu-id="96cfa-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96cfa-136">RELATED LINKS</span></span>
