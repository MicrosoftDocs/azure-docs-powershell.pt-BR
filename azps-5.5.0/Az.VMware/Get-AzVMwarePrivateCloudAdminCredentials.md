---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 7502bbd96371aa505d8d927dfb9a491c2ca32b34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118512"
---
# <span data-ttu-id="0fc0e-101">Get-AzVMwarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="0fc0e-101">Get-AzVMwarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="0fc0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fc0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc0e-103">Listar as credenciais de administrador para a nuvem privada</span><span class="sxs-lookup"><span data-stu-id="0fc0e-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="0fc0e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fc0e-104">SYNTAX</span></span>

```
Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fc0e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0fc0e-105">DESCRIPTION</span></span>
<span data-ttu-id="0fc0e-106">Listar as credenciais de administrador para a nuvem privada</span><span class="sxs-lookup"><span data-stu-id="0fc0e-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="0fc0e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0fc0e-107">EXAMPLES</span></span>

### <span data-ttu-id="0fc0e-108">Exemplo 1: Obter credencial de administrador da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="0fc0e-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="0fc0e-109">Obter credencial de administrador da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="0fc0e-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="0fc0e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fc0e-110">PARAMETERS</span></span>

### <span data-ttu-id="0fc0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc0e-111">-DefaultProfile</span></span>
<span data-ttu-id="0fc0e-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc0e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc0e-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0fc0e-113">-PrivateCloudName</span></span>
<span data-ttu-id="0fc0e-114">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="0fc0e-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="0fc0e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc0e-115">-ResourceGroupName</span></span>
<span data-ttu-id="0fc0e-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0fc0e-116">The name of the resource group.</span></span>
<span data-ttu-id="0fc0e-117">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0fc0e-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0fc0e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fc0e-118">-SubscriptionId</span></span>
<span data-ttu-id="0fc0e-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0fc0e-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0fc0e-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0fc0e-120">-Confirm</span></span>
<span data-ttu-id="0fc0e-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fc0e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc0e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc0e-122">-WhatIf</span></span>
<span data-ttu-id="0fc0e-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0fc0e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc0e-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0fc0e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc0e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc0e-125">CommonParameters</span></span>
<span data-ttu-id="0fc0e-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc0e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc0e-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fc0e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc0e-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="0fc0e-128">INPUTS</span></span>

## <span data-ttu-id="0fc0e-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="0fc0e-129">OUTPUTS</span></span>

### <span data-ttu-id="0fc0e-130">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="0fc0e-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="0fc0e-131">Notas</span><span class="sxs-lookup"><span data-stu-id="0fc0e-131">NOTES</span></span>

<span data-ttu-id="0fc0e-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="0fc0e-132">ALIASES</span></span>

## <span data-ttu-id="0fc0e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fc0e-133">RELATED LINKS</span></span>

