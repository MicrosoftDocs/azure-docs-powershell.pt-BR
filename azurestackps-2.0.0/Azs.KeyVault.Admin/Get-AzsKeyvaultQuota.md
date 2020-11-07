---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776001"
---
# <span data-ttu-id="b4035-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="b4035-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="b4035-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4035-102">SYNOPSIS</span></span>
<span data-ttu-id="b4035-103">Obter uma lista de todos os objetos de cota para o keyvault em um local.</span><span class="sxs-lookup"><span data-stu-id="b4035-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="b4035-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4035-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4035-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4035-105">DESCRIPTION</span></span>
<span data-ttu-id="b4035-106">Obter uma lista de todos os objetos de cota para o keyvault em um local.</span><span class="sxs-lookup"><span data-stu-id="b4035-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="b4035-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4035-107">EXAMPLES</span></span>

### <span data-ttu-id="b4035-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="b4035-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="b4035-109">Obter uma lista de todos os objetos de cota para o keyvault em um local.</span><span class="sxs-lookup"><span data-stu-id="b4035-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="b4035-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4035-110">PARAMETERS</span></span>

### <span data-ttu-id="b4035-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4035-111">-DefaultProfile</span></span>
<span data-ttu-id="b4035-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4035-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b4035-113">-Local</span><span class="sxs-lookup"><span data-stu-id="b4035-113">-Location</span></span>
<span data-ttu-id="b4035-114">O local da cota.</span><span class="sxs-lookup"><span data-stu-id="b4035-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b4035-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4035-115">-SubscriptionId</span></span>
<span data-ttu-id="b4035-116">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b4035-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b4035-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4035-117">CommonParameters</span></span>
<span data-ttu-id="b4035-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4035-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4035-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4035-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4035-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4035-120">INPUTS</span></span>

## <span data-ttu-id="b4035-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4035-121">OUTPUTS</span></span>

### <span data-ttu-id="b4035-122">Microsoft. Azure. PowerShell. cmdlets. KeyVaultAdmin. Models. Api20170201Preview. IQuota</span><span class="sxs-lookup"><span data-stu-id="b4035-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="b4035-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4035-123">NOTES</span></span>

## <span data-ttu-id="b4035-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4035-124">RELATED LINKS</span></span>

