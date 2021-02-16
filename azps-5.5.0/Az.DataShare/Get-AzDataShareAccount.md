---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113246"
---
# <span data-ttu-id="9205d-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="9205d-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="9205d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9205d-102">SYNOPSIS</span></span>
<span data-ttu-id="9205d-103">Obtém informações sobre Contas DataShare</span><span class="sxs-lookup"><span data-stu-id="9205d-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="9205d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9205d-104">SYNTAX</span></span>

### <span data-ttu-id="9205d-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9205d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9205d-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9205d-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9205d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9205d-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9205d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9205d-108">DESCRIPTION</span></span>
<span data-ttu-id="9205d-109">O **cmdlet Get-AzDataShareAccount** obtém informações sobre contas da ltda em um grupo de recursos/assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9205d-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="9205d-110">Se você especificar o nome de uma conta, esse cmdlet obterá informações sobre essa conta de datshare.</span><span class="sxs-lookup"><span data-stu-id="9205d-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="9205d-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as contas de dados em uma assinatura do Azure/grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9205d-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="9205d-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9205d-112">EXAMPLES</span></span>

### <span data-ttu-id="9205d-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9205d-113">Example 1</span></span>
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

<span data-ttu-id="9205d-114">Esse comando exibe informações sobre todas as contas de domínio na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9205d-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="9205d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9205d-115">PARAMETERS</span></span>

### <span data-ttu-id="9205d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9205d-116">-DefaultProfile</span></span>
<span data-ttu-id="9205d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9205d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9205d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9205d-118">-Name</span></span>
<span data-ttu-id="9205d-119">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="9205d-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="9205d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9205d-120">-ResourceGroupName</span></span>
<span data-ttu-id="9205d-121">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="9205d-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="9205d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9205d-122">-ResourceId</span></span>
<span data-ttu-id="9205d-123">A ID do recurso da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="9205d-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="9205d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9205d-124">CommonParameters</span></span>
<span data-ttu-id="9205d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9205d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9205d-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9205d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9205d-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="9205d-127">INPUTS</span></span>

### <span data-ttu-id="9205d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9205d-128">System.String</span></span>

## <span data-ttu-id="9205d-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="9205d-129">OUTPUTS</span></span>

### <span data-ttu-id="9205d-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="9205d-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="9205d-131">Notas</span><span class="sxs-lookup"><span data-stu-id="9205d-131">NOTES</span></span>

## <span data-ttu-id="9205d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9205d-132">RELATED LINKS</span></span>
