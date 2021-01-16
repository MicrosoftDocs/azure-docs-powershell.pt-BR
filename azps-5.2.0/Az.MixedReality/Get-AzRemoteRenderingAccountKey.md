---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257435"
---
# <span data-ttu-id="33551-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="33551-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="33551-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33551-102">SYNOPSIS</span></span>
<span data-ttu-id="33551-103">Obter chaves da conta de renderização remota</span><span class="sxs-lookup"><span data-stu-id="33551-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="33551-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33551-104">SYNTAX</span></span>

### <span data-ttu-id="33551-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="33551-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33551-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33551-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33551-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="33551-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33551-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33551-108">DESCRIPTION</span></span>
<span data-ttu-id="33551-109">Obter as chaves de desenvolvedor da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="33551-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="33551-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33551-110">EXAMPLES</span></span>

### <span data-ttu-id="33551-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33551-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="33551-112">Obter as chaves de desenvolvedor da conta de renderização remota "exemplo" da assinatura atual e do grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="33551-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="33551-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="33551-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="33551-114">Obter as chaves de desenvolvedor da conta de renderização remota "exemplo" da assinatura atual e do grupo de recursos "Rg1" com o encanamento.</span><span class="sxs-lookup"><span data-stu-id="33551-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="33551-115">OS</span><span class="sxs-lookup"><span data-stu-id="33551-115">PARAMETERS</span></span>

### <span data-ttu-id="33551-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33551-116">-DefaultProfile</span></span>
<span data-ttu-id="33551-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33551-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33551-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33551-118">-InputObject</span></span>
<span data-ttu-id="33551-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="33551-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33551-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="33551-120">-Name</span></span>
<span data-ttu-id="33551-121">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="33551-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33551-122">-ResourceGroupName</span></span>
<span data-ttu-id="33551-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="33551-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33551-124">-ResourceId</span></span>
<span data-ttu-id="33551-125">ID do recurso da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="33551-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33551-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33551-126">CommonParameters</span></span>
<span data-ttu-id="33551-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33551-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="33551-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33551-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33551-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33551-129">INPUTS</span></span>

### <span data-ttu-id="33551-130">System. String</span><span class="sxs-lookup"><span data-stu-id="33551-130">System.String</span></span>

### <span data-ttu-id="33551-131">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="33551-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="33551-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33551-132">OUTPUTS</span></span>

### <span data-ttu-id="33551-133">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="33551-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="33551-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33551-134">NOTES</span></span>

## <span data-ttu-id="33551-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33551-135">RELATED LINKS</span></span>
