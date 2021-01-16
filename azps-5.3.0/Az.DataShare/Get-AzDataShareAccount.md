---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271506"
---
# <span data-ttu-id="5eb0d-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="5eb0d-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="5eb0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5eb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb0d-103">Obtém informações sobre contas de compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="5eb0d-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="5eb0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5eb0d-104">SYNTAX</span></span>

### <span data-ttu-id="5eb0d-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5eb0d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eb0d-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5eb0d-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5eb0d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5eb0d-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eb0d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5eb0d-108">DESCRIPTION</span></span>
<span data-ttu-id="5eb0d-109">O cmdlet **Get-AzDataShareAccount** Obtém informações sobre contas de compartilhamento de dados em um grupo de recursos/assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="5eb0d-110">Se você especificar o nome de uma conta, esse cmdlet obterá informações sobre essa conta do datshare.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="5eb0d-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as contas de compartilhamento de dados em um grupo de recursos/assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="5eb0d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5eb0d-112">EXAMPLES</span></span>

### <span data-ttu-id="5eb0d-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5eb0d-113">Example 1</span></span>
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

<span data-ttu-id="5eb0d-114">Esse comando exibe informações sobre todas as contas de compartilhamento de dados na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="5eb0d-115">OS</span><span class="sxs-lookup"><span data-stu-id="5eb0d-115">PARAMETERS</span></span>

### <span data-ttu-id="5eb0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb0d-116">-DefaultProfile</span></span>
<span data-ttu-id="5eb0d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb0d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5eb0d-118">-Name</span></span>
<span data-ttu-id="5eb0d-119">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="5eb0d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb0d-120">-ResourceGroupName</span></span>
<span data-ttu-id="5eb0d-121">O nome do grupo de recursos da conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="5eb0d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5eb0d-122">-ResourceId</span></span>
<span data-ttu-id="5eb0d-123">A ID do recurso da conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="5eb0d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb0d-124">CommonParameters</span></span>
<span data-ttu-id="5eb0d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb0d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb0d-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5eb0d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb0d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5eb0d-127">INPUTS</span></span>

### <span data-ttu-id="5eb0d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5eb0d-128">System.String</span></span>

## <span data-ttu-id="5eb0d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5eb0d-129">OUTPUTS</span></span>

### <span data-ttu-id="5eb0d-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="5eb0d-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="5eb0d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5eb0d-131">NOTES</span></span>

## <span data-ttu-id="5eb0d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eb0d-132">RELATED LINKS</span></span>
