---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941863"
---
# <span data-ttu-id="e4e93-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4e93-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="e4e93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4e93-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e93-103">Obtém as chaves de API para uma conta.</span><span class="sxs-lookup"><span data-stu-id="e4e93-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="e4e93-104">Essas chaves são o mecanismo de autenticação usado em chamadas subsequentes para mapas do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e93-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="e4e93-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4e93-105">SYNTAX</span></span>

### <span data-ttu-id="e4e93-106">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4e93-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4e93-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4e93-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4e93-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4e93-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4e93-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4e93-109">DESCRIPTION</span></span>
<span data-ttu-id="e4e93-110">O cmdlet Get-AzMapsAccountKey Obtém as chaves de API para uma conta provisionada do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="e4e93-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="e4e93-111">Uma conta do Azure Maps tem duas chaves de API: primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="e4e93-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="e4e93-112">As chaves permitem a interação com o ponto de extremidade da conta do Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="e4e93-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="e4e93-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey. MD) para gerar novamente uma chave.</span><span class="sxs-lookup"><span data-stu-id="e4e93-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="e4e93-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4e93-114">EXAMPLES</span></span>

### <span data-ttu-id="e4e93-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4e93-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="e4e93-116">Retorna as chaves da conta chamada myaccount no grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4e93-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e4e93-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4e93-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="e4e93-118">Retorna as chaves da conta do Azure Maps especificada.</span><span class="sxs-lookup"><span data-stu-id="e4e93-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="e4e93-119">OS</span><span class="sxs-lookup"><span data-stu-id="e4e93-119">PARAMETERS</span></span>

### <span data-ttu-id="e4e93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e93-120">-DefaultProfile</span></span>
<span data-ttu-id="e4e93-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e93-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4e93-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4e93-122">-InputObject</span></span>
<span data-ttu-id="e4e93-123">Mapeia a conta canalizada do Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="e4e93-123">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e93-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4e93-124">-Name</span></span>
<span data-ttu-id="e4e93-125">Mapeia o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="e4e93-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e93-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e93-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4e93-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4e93-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e93-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4e93-128">-ResourceId</span></span>
<span data-ttu-id="e4e93-129">Mapeia ResourceId de conta.</span><span class="sxs-lookup"><span data-stu-id="e4e93-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="e4e93-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e93-130">CommonParameters</span></span>
<span data-ttu-id="e4e93-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e93-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e93-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e93-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e93-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4e93-133">INPUTS</span></span>

### <span data-ttu-id="e4e93-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e4e93-134">System.String</span></span>

### <span data-ttu-id="e4e93-135">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e4e93-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="e4e93-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4e93-136">OUTPUTS</span></span>

### <span data-ttu-id="e4e93-137">Microsoft. Azure. Commands. Maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e4e93-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="e4e93-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4e93-138">NOTES</span></span>

## <span data-ttu-id="e4e93-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4e93-139">RELATED LINKS</span></span>
