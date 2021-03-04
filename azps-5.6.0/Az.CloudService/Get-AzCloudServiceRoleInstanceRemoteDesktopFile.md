---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 74948fe91e4a2823c9bbe8e8c0e50ade33612e18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890479"
---
# <span data-ttu-id="54c47-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="54c47-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="54c47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c47-102">SYNOPSIS</span></span>
<span data-ttu-id="54c47-103">Obtém um arquivo de área de trabalho remota para uma instância de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="54c47-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="54c47-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="54c47-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="54c47-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="54c47-105">DESCRIPTION</span></span>
<span data-ttu-id="54c47-106">Obtém um arquivo de área de trabalho remota para uma instância de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="54c47-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="54c47-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54c47-107">EXAMPLES</span></span>

### <span data-ttu-id="54c47-108">Exemplo 1: Obter um arquivo RDP</span><span class="sxs-lookup"><span data-stu-id="54c47-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="54c47-109">Este comando obtém um arquivo RDP para a instância de função chamada ContosoFrontEnd IN 0 do Serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos \_ \_ chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="54c47-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="54c47-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="54c47-110">PARAMETERS</span></span>

### <span data-ttu-id="54c47-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="54c47-111">-CloudServiceName</span></span>
<span data-ttu-id="54c47-112">.</span><span class="sxs-lookup"><span data-stu-id="54c47-112">.</span></span>

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

### <span data-ttu-id="54c47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c47-113">-DefaultProfile</span></span>
<span data-ttu-id="54c47-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54c47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c47-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="54c47-115">-OutFile</span></span>
<span data-ttu-id="54c47-116">Caminho para gravar arquivo de saída para</span><span class="sxs-lookup"><span data-stu-id="54c47-116">Path to write output file to</span></span>

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

### <span data-ttu-id="54c47-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54c47-117">-PassThru</span></span>
<span data-ttu-id="54c47-118">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="54c47-118">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c47-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c47-119">-ResourceGroupName</span></span>
<span data-ttu-id="54c47-120">.</span><span class="sxs-lookup"><span data-stu-id="54c47-120">.</span></span>

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

### <span data-ttu-id="54c47-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="54c47-121">-RoleInstanceName</span></span>
<span data-ttu-id="54c47-122">Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="54c47-122">Name of the role instance.</span></span>

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

### <span data-ttu-id="54c47-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54c47-123">-SubscriptionId</span></span>
<span data-ttu-id="54c47-124">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="54c47-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="54c47-125">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="54c47-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="54c47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c47-126">CommonParameters</span></span>
<span data-ttu-id="54c47-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c47-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54c47-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c47-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54c47-129">INPUTS</span></span>

## <span data-ttu-id="54c47-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="54c47-130">OUTPUTS</span></span>

### <span data-ttu-id="54c47-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54c47-131">System.Boolean</span></span>

## <span data-ttu-id="54c47-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="54c47-132">NOTES</span></span>

<span data-ttu-id="54c47-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="54c47-133">ALIASES</span></span>

## <span data-ttu-id="54c47-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54c47-134">RELATED LINKS</span></span>

