---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 0b61764d358cc234f66dc8bb24249ca93a4e9919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115232"
---
# <span data-ttu-id="27867-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="27867-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="27867-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27867-102">SYNOPSIS</span></span>
<span data-ttu-id="27867-103">Criar conta de âncoras de espaço espaço</span><span class="sxs-lookup"><span data-stu-id="27867-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="27867-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27867-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27867-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="27867-105">DESCRIPTION</span></span>
<span data-ttu-id="27867-106">Crie uma nova Conta de Âncoras Desaportivas em determinada Assinatura, Grupo de Recursos e Região.</span><span class="sxs-lookup"><span data-stu-id="27867-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="27867-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27867-107">EXAMPLES</span></span>

### <span data-ttu-id="27867-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="27867-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="27867-109">Crie um novo "exemplo" de conta de âncoras de espaço reservado na assinatura atual, grupo de recursos "rg1" e Central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="27867-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="27867-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27867-110">PARAMETERS</span></span>

### <span data-ttu-id="27867-111">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="27867-111">-Confirm</span></span>
<span data-ttu-id="27867-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27867-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27867-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27867-113">-DefaultProfile</span></span>
<span data-ttu-id="27867-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27867-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27867-115">-Local</span><span class="sxs-lookup"><span data-stu-id="27867-115">-Location</span></span>
<span data-ttu-id="27867-116">Localização da conta de âncoras locais.</span><span class="sxs-lookup"><span data-stu-id="27867-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27867-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="27867-117">-Name</span></span>
<span data-ttu-id="27867-118">Nome da conta De âncoras de espaço.</span><span class="sxs-lookup"><span data-stu-id="27867-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27867-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27867-119">-ResourceGroupName</span></span>
<span data-ttu-id="27867-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27867-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27867-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27867-121">-WhatIf</span></span>
<span data-ttu-id="27867-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="27867-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27867-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27867-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27867-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27867-124">CommonParameters</span></span>
<span data-ttu-id="27867-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27867-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="27867-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27867-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27867-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="27867-127">INPUTS</span></span>

### <span data-ttu-id="27867-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="27867-128">None</span></span>

## <span data-ttu-id="27867-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="27867-129">OUTPUTS</span></span>

### <span data-ttu-id="27867-130">Microsoft.Azure.Commands.MixedReality.GeoespaciaisAccount.PSSárialEstaresAccount</span><span class="sxs-lookup"><span data-stu-id="27867-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="27867-131">Notas</span><span class="sxs-lookup"><span data-stu-id="27867-131">NOTES</span></span>

## <span data-ttu-id="27867-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27867-132">RELATED LINKS</span></span>
