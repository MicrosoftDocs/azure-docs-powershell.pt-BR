---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: df65bd7b8dfd2f3091590b8830059965e599c029
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888351"
---
# <span data-ttu-id="77aad-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="77aad-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="77aad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77aad-102">SYNOPSIS</span></span>
<span data-ttu-id="77aad-103">Criar conta de renderização remota</span><span class="sxs-lookup"><span data-stu-id="77aad-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="77aad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="77aad-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77aad-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="77aad-105">DESCRIPTION</span></span>
<span data-ttu-id="77aad-106">Crie uma nova conta de renderização remota em determinada Assinatura, Grupo de Recursos e Região.</span><span class="sxs-lookup"><span data-stu-id="77aad-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="77aad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77aad-107">EXAMPLES</span></span>

### <span data-ttu-id="77aad-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77aad-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="77aad-109">Crie um novo "exemplo" de Conta de Renderização Remota na Assinatura atual, Grupo de Recursos "rg1" e Central US.</span><span class="sxs-lookup"><span data-stu-id="77aad-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="77aad-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="77aad-110">PARAMETERS</span></span>

### <span data-ttu-id="77aad-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77aad-111">-Confirm</span></span>
<span data-ttu-id="77aad-112">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77aad-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77aad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77aad-113">-DefaultProfile</span></span>
<span data-ttu-id="77aad-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77aad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77aad-115">-Location</span><span class="sxs-lookup"><span data-stu-id="77aad-115">-Location</span></span>
<span data-ttu-id="77aad-116">Local da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="77aad-116">Remote Rendering Account Location.</span></span>

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

### <span data-ttu-id="77aad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="77aad-117">-Name</span></span>
<span data-ttu-id="77aad-118">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="77aad-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77aad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77aad-119">-ResourceGroupName</span></span>
<span data-ttu-id="77aad-120">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="77aad-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="77aad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77aad-121">-WhatIf</span></span>
<span data-ttu-id="77aad-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77aad-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77aad-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77aad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77aad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77aad-124">CommonParameters</span></span>
<span data-ttu-id="77aad-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77aad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="77aad-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77aad-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77aad-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77aad-127">INPUTS</span></span>

### <span data-ttu-id="77aad-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="77aad-128">None</span></span>

## <span data-ttu-id="77aad-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="77aad-129">OUTPUTS</span></span>

### <span data-ttu-id="77aad-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="77aad-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="77aad-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="77aad-131">NOTES</span></span>

## <span data-ttu-id="77aad-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77aad-132">RELATED LINKS</span></span>
