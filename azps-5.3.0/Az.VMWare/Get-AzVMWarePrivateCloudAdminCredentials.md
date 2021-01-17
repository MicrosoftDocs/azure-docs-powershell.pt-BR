---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427862"
---
# <span data-ttu-id="6cd0b-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="6cd0b-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="6cd0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cd0b-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd0b-103">Listar as credenciais de administrador para a nuvem privada</span><span class="sxs-lookup"><span data-stu-id="6cd0b-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="6cd0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cd0b-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cd0b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cd0b-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd0b-106">Listar as credenciais de administrador para a nuvem privada</span><span class="sxs-lookup"><span data-stu-id="6cd0b-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="6cd0b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cd0b-107">EXAMPLES</span></span>

### <span data-ttu-id="6cd0b-108">Exemplo 1: obter as credenciais de administrador da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="6cd0b-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="6cd0b-109">Obter credenciais de administrador da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="6cd0b-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="6cd0b-110">OS</span><span class="sxs-lookup"><span data-stu-id="6cd0b-110">PARAMETERS</span></span>

### <span data-ttu-id="6cd0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd0b-111">-DefaultProfile</span></span>
<span data-ttu-id="6cd0b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cd0b-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="6cd0b-113">-PrivateCloudName</span></span>
<span data-ttu-id="6cd0b-114">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="6cd0b-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="6cd0b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd0b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6cd0b-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-116">The name of the resource group.</span></span>
<span data-ttu-id="6cd0b-117">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6cd0b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cd0b-118">-SubscriptionId</span></span>
<span data-ttu-id="6cd0b-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6cd0b-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cd0b-120">-Confirm</span></span>
<span data-ttu-id="6cd0b-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd0b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd0b-122">-WhatIf</span></span>
<span data-ttu-id="6cd0b-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cd0b-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd0b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd0b-125">CommonParameters</span></span>
<span data-ttu-id="6cd0b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd0b-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cd0b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd0b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cd0b-128">INPUTS</span></span>

## <span data-ttu-id="6cd0b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cd0b-129">OUTPUTS</span></span>

### <span data-ttu-id="6cd0b-130">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="6cd0b-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="6cd0b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cd0b-131">NOTES</span></span>

<span data-ttu-id="6cd0b-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6cd0b-132">ALIASES</span></span>

## <span data-ttu-id="6cd0b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cd0b-133">RELATED LINKS</span></span>

