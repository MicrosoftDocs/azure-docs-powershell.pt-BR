---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945282"
---
# <span data-ttu-id="8f583-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="8f583-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="8f583-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f583-102">SYNOPSIS</span></span>
<span data-ttu-id="8f583-103">Retorna as configurações do provedor de recursos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f583-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="8f583-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f583-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f583-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f583-105">DESCRIPTION</span></span>
<span data-ttu-id="8f583-106">Retorna as configurações do provedor de recursos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f583-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="8f583-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f583-107">EXAMPLES</span></span>

### <span data-ttu-id="8f583-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="8f583-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="8f583-109">Obter as configurações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f583-109">Get the storage settings.</span></span>

## <span data-ttu-id="8f583-110">OS</span><span class="sxs-lookup"><span data-stu-id="8f583-110">PARAMETERS</span></span>

### <span data-ttu-id="8f583-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f583-111">-DefaultProfile</span></span>
<span data-ttu-id="8f583-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f583-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f583-113">-Local</span><span class="sxs-lookup"><span data-stu-id="8f583-113">-Location</span></span>
<span data-ttu-id="8f583-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8f583-114">Resource location.</span></span>

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

### <span data-ttu-id="8f583-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f583-115">-SubscriptionId</span></span>
<span data-ttu-id="8f583-116">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="8f583-116">Subscription Id.</span></span>

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

### <span data-ttu-id="8f583-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f583-117">CommonParameters</span></span>
<span data-ttu-id="8f583-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f583-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f583-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f583-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f583-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f583-120">INPUTS</span></span>

## <span data-ttu-id="8f583-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f583-121">OUTPUTS</span></span>

### <span data-ttu-id="8f583-122">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="8f583-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="8f583-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f583-123">NOTES</span></span>

## <span data-ttu-id="8f583-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f583-124">RELATED LINKS</span></span>

