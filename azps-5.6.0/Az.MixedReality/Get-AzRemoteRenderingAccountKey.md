---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: 03cb387b77dc2f003277b9f04a482f88a8da86fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886220"
---
# <span data-ttu-id="4307e-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="4307e-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="4307e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4307e-102">SYNOPSIS</span></span>
<span data-ttu-id="4307e-103">Obter chaves da Conta de Renderização Remota</span><span class="sxs-lookup"><span data-stu-id="4307e-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="4307e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4307e-104">SYNTAX</span></span>

### <span data-ttu-id="4307e-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4307e-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4307e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4307e-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4307e-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="4307e-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4307e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4307e-108">DESCRIPTION</span></span>
<span data-ttu-id="4307e-109">Obter chaves de desenvolvedor da Conta de Renderização Remota.</span><span class="sxs-lookup"><span data-stu-id="4307e-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="4307e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4307e-110">EXAMPLES</span></span>

### <span data-ttu-id="4307e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4307e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="4307e-112">Obter chaves de desenvolvedor do "exemplo" da Conta de Renderização Remota do Grupo de Recursos e Assinatura atual "rg1".</span><span class="sxs-lookup"><span data-stu-id="4307e-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="4307e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4307e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="4307e-114">Obter chaves de desenvolvedor do "exemplo" da Conta de Renderização Remota do Grupo de Recursos e Assinatura atual "rg1" com canalização.</span><span class="sxs-lookup"><span data-stu-id="4307e-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="4307e-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4307e-115">PARAMETERS</span></span>

### <span data-ttu-id="4307e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4307e-116">-DefaultProfile</span></span>
<span data-ttu-id="4307e-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4307e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4307e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4307e-118">-InputObject</span></span>
<span data-ttu-id="4307e-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="4307e-119">The custom domain object.</span></span>

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

### <span data-ttu-id="4307e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4307e-120">-Name</span></span>
<span data-ttu-id="4307e-121">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="4307e-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="4307e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4307e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4307e-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="4307e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="4307e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4307e-124">-ResourceId</span></span>
<span data-ttu-id="4307e-125">ID de recurso da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="4307e-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="4307e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4307e-126">CommonParameters</span></span>
<span data-ttu-id="4307e-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4307e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4307e-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4307e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4307e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4307e-129">INPUTS</span></span>

### <span data-ttu-id="4307e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4307e-130">System.String</span></span>

### <span data-ttu-id="4307e-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="4307e-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="4307e-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4307e-132">OUTPUTS</span></span>

### <span data-ttu-id="4307e-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4307e-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="4307e-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="4307e-134">NOTES</span></span>

## <span data-ttu-id="4307e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4307e-135">RELATED LINKS</span></span>
