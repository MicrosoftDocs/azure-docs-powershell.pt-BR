---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256865"
---
# <span data-ttu-id="4720a-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="4720a-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="4720a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4720a-102">SYNOPSIS</span></span>
<span data-ttu-id="4720a-103">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="4720a-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="4720a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4720a-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4720a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4720a-105">DESCRIPTION</span></span>
<span data-ttu-id="4720a-106">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="4720a-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="4720a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4720a-107">EXAMPLES</span></span>

### <span data-ttu-id="4720a-108">Exemplo 1: listar todo o BD de réplica em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="4720a-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4720a-109">Esse comando lista todos os bancos de BD de réplica em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="4720a-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="4720a-110">OS</span><span class="sxs-lookup"><span data-stu-id="4720a-110">PARAMETERS</span></span>

### <span data-ttu-id="4720a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4720a-111">-DefaultProfile</span></span>
<span data-ttu-id="4720a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4720a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4720a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4720a-113">-ResourceGroupName</span></span>
<span data-ttu-id="4720a-114">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="4720a-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4720a-115">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="4720a-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4720a-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4720a-116">-ServerName</span></span>
<span data-ttu-id="4720a-117">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4720a-117">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4720a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4720a-118">-SubscriptionId</span></span>
<span data-ttu-id="4720a-119">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4720a-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4720a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4720a-120">CommonParameters</span></span>
<span data-ttu-id="4720a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4720a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4720a-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4720a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4720a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4720a-123">INPUTS</span></span>

## <span data-ttu-id="4720a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4720a-124">OUTPUTS</span></span>

### <span data-ttu-id="4720a-125">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="4720a-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="4720a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4720a-126">NOTES</span></span>

<span data-ttu-id="4720a-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4720a-127">ALIASES</span></span>

## <span data-ttu-id="4720a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4720a-128">RELATED LINKS</span></span>

