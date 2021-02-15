---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
ms.openlocfilehash: 9d4faa4a51352902330286722a005fae1b42bef7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115242"
---
# <span data-ttu-id="953f1-101">Get-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="953f1-101">Get-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="953f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="953f1-102">SYNOPSIS</span></span>
<span data-ttu-id="953f1-103">Obter Conta de Renderização Remota</span><span class="sxs-lookup"><span data-stu-id="953f1-103">Get Remote Rendering Account</span></span>

## <span data-ttu-id="953f1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="953f1-104">SYNTAX</span></span>

### <span data-ttu-id="953f1-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="953f1-105">ListParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="953f1-106">GetParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="953f1-106">GetParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="953f1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="953f1-107">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="953f1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="953f1-108">DESCRIPTION</span></span>
<span data-ttu-id="953f1-109">Obter ou listar As Contas de Renderização Remota em determinados Grupos de Recursos e Assinaturas.</span><span class="sxs-lookup"><span data-stu-id="953f1-109">Get or list Remote Rendering Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="953f1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="953f1-110">EXAMPLES</span></span>

### <span data-ttu-id="953f1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="953f1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/RemoteRenderingAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="953f1-112">Liste todas as Contas de Renderização Remota no Grupo de Recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="953f1-112">List all Remote Rendering Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="953f1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="953f1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="953f1-114">Obter "exemplo" de Conta de Renderização Remota no Grupo de Recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="953f1-114">Get Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="953f1-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="953f1-115">PARAMETERS</span></span>

### <span data-ttu-id="953f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953f1-116">-DefaultProfile</span></span>
<span data-ttu-id="953f1-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="953f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="953f1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="953f1-118">-Name</span></span>
<span data-ttu-id="953f1-119">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="953f1-119">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953f1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="953f1-120">-ResourceGroupName</span></span>
<span data-ttu-id="953f1-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="953f1-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953f1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="953f1-122">-ResourceId</span></span>
<span data-ttu-id="953f1-123">ID do Recurso da Conta de Renderização Remota.</span><span class="sxs-lookup"><span data-stu-id="953f1-123">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="953f1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953f1-124">CommonParameters</span></span>
<span data-ttu-id="953f1-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="953f1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="953f1-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="953f1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953f1-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="953f1-127">INPUTS</span></span>

### <span data-ttu-id="953f1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="953f1-128">System.String</span></span>

## <span data-ttu-id="953f1-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="953f1-129">OUTPUTS</span></span>

### <span data-ttu-id="953f1-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoterenderingAccount</span><span class="sxs-lookup"><span data-stu-id="953f1-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="953f1-131">Notas</span><span class="sxs-lookup"><span data-stu-id="953f1-131">NOTES</span></span>

## <span data-ttu-id="953f1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="953f1-132">RELATED LINKS</span></span>
