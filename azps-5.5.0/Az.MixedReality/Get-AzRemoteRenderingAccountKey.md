---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115240"
---
# <span data-ttu-id="581c5-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="581c5-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="581c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="581c5-102">SYNOPSIS</span></span>
<span data-ttu-id="581c5-103">Obter chaves da Conta de Renderização Remota</span><span class="sxs-lookup"><span data-stu-id="581c5-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="581c5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="581c5-104">SYNTAX</span></span>

### <span data-ttu-id="581c5-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="581c5-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="581c5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="581c5-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="581c5-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="581c5-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="581c5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="581c5-108">DESCRIPTION</span></span>
<span data-ttu-id="581c5-109">Obter chaves de desenvolvedor da Conta de Renderização Remota.</span><span class="sxs-lookup"><span data-stu-id="581c5-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="581c5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="581c5-110">EXAMPLES</span></span>

### <span data-ttu-id="581c5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="581c5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="581c5-112">Obter chaves de desenvolvedor da Conta de Renderização Remota "exemplo" da assinatura atual e grupo de recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="581c5-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="581c5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="581c5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="581c5-114">Obter chaves de desenvolvedor da Conta de Renderização Remota "exemplo" da assinatura atual e grupo de recursos "rg1" com piping.</span><span class="sxs-lookup"><span data-stu-id="581c5-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="581c5-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="581c5-115">PARAMETERS</span></span>

### <span data-ttu-id="581c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581c5-116">-DefaultProfile</span></span>
<span data-ttu-id="581c5-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="581c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="581c5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="581c5-118">-InputObject</span></span>
<span data-ttu-id="581c5-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="581c5-119">The custom domain object.</span></span>

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

### <span data-ttu-id="581c5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="581c5-120">-Name</span></span>
<span data-ttu-id="581c5-121">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="581c5-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="581c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="581c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="581c5-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="581c5-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="581c5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="581c5-124">-ResourceId</span></span>
<span data-ttu-id="581c5-125">ID do Recurso da Conta de Renderização Remota.</span><span class="sxs-lookup"><span data-stu-id="581c5-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="581c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581c5-126">CommonParameters</span></span>
<span data-ttu-id="581c5-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="581c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="581c5-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="581c5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581c5-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="581c5-129">INPUTS</span></span>

### <span data-ttu-id="581c5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="581c5-130">System.String</span></span>

### <span data-ttu-id="581c5-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoterenderingAccount</span><span class="sxs-lookup"><span data-stu-id="581c5-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="581c5-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="581c5-132">OUTPUTS</span></span>

### <span data-ttu-id="581c5-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="581c5-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="581c5-134">Notas</span><span class="sxs-lookup"><span data-stu-id="581c5-134">NOTES</span></span>

## <span data-ttu-id="581c5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="581c5-135">RELATED LINKS</span></span>
