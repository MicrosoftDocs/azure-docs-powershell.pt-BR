---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 7b47e54076441f1f4e78ec8cabc6a9dd3cd47153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885727"
---
# <span data-ttu-id="f7b44-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="f7b44-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="f7b44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b44-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b44-103">Obtém informações sobre contas DataShare</span><span class="sxs-lookup"><span data-stu-id="f7b44-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="f7b44-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7b44-104">SYNTAX</span></span>

### <span data-ttu-id="f7b44-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f7b44-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7b44-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b44-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7b44-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b44-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7b44-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7b44-108">DESCRIPTION</span></span>
<span data-ttu-id="f7b44-109">O cmdlet **Get-AzDataShareAccount** obtém informações sobre contas daiáculas em um grupo de assinatura/recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b44-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="f7b44-110">Se você especificar o nome de uma conta, esse cmdlet obterá informações sobre essa conta de datshare.</span><span class="sxs-lookup"><span data-stu-id="f7b44-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="f7b44-111">Se você não especificar um nome, este cmdlet obterá informações sobre todas as contas de datashare em um grupo de assinatura/recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b44-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="f7b44-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7b44-112">EXAMPLES</span></span>

### <span data-ttu-id="f7b44-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7b44-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="f7b44-114">Este comando exibe informações sobre todas as contas de datashare na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b44-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="f7b44-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7b44-115">PARAMETERS</span></span>

### <span data-ttu-id="f7b44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b44-116">-DefaultProfile</span></span>
<span data-ttu-id="f7b44-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7b44-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f7b44-118">-Name</span></span>
<span data-ttu-id="f7b44-119">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b44-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b44-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b44-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7b44-121">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="f7b44-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b44-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7b44-122">-ResourceId</span></span>
<span data-ttu-id="f7b44-123">A id de recurso da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="f7b44-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b44-124">CommonParameters</span></span>
<span data-ttu-id="f7b44-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b44-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7b44-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b44-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7b44-127">INPUTS</span></span>

### <span data-ttu-id="f7b44-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f7b44-128">System.String</span></span>

## <span data-ttu-id="f7b44-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7b44-129">OUTPUTS</span></span>

### <span data-ttu-id="f7b44-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="f7b44-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="f7b44-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7b44-131">NOTES</span></span>

## <span data-ttu-id="f7b44-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7b44-132">RELATED LINKS</span></span>
