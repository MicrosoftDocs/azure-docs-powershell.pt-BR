---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 61c5fc7f80ab157724156d86a5cbb8df8bb23841
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595729"
---
# <span data-ttu-id="467a1-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="467a1-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="467a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="467a1-102">SYNOPSIS</span></span>
<span data-ttu-id="467a1-103">Cria um novo servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="467a1-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="467a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="467a1-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="467a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="467a1-105">DESCRIPTION</span></span>
<span data-ttu-id="467a1-106">O cmdlet New-AzAnalysisServicesServer cria um novo servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="467a1-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="467a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="467a1-107">EXAMPLES</span></span>

### <span data-ttu-id="467a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="467a1-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="467a1-109">Cria um servidor chamado TestServer na região do Azure West-US e no grupo de recursos testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="467a1-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="467a1-110">O nível de SKU do servidor será S1.</span><span class="sxs-lookup"><span data-stu-id="467a1-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="467a1-111">OS</span><span class="sxs-lookup"><span data-stu-id="467a1-111">PARAMETERS</span></span>

### <span data-ttu-id="467a1-112">-Administrador</span><span class="sxs-lookup"><span data-stu-id="467a1-112">-Administrator</span></span>
<span data-ttu-id="467a1-113">Uma cadeia de caracteres que representa uma lista separada por vírgulas de usuários ou grupos a serem definidos como administradores no servidor.</span><span class="sxs-lookup"><span data-stu-id="467a1-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="467a1-114">Os usuários ou grupos precisam ser do formato UPN especificado, por exemplo, user@contoso.com ou groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="467a1-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="467a1-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="467a1-116">O URI do contêiner de BLOB para fazer backup do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="467a1-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-117">-Defaultconnectionmode</span><span class="sxs-lookup"><span data-stu-id="467a1-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="467a1-118">Modo de conexão padrão de um servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="467a1-118">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467a1-119">-DefaultProfile</span></span>
<span data-ttu-id="467a1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="467a1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="467a1-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="467a1-121">-FirewallConfig</span></span>
<span data-ttu-id="467a1-122">Configuração de firewall de um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="467a1-122">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="467a1-123">-GatewayResourceId</span></span>
<span data-ttu-id="467a1-124">ID do recurso do gateway para assocaite para um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="467a1-124">Gateway resource Id for assocaite to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-125">-Local</span><span class="sxs-lookup"><span data-stu-id="467a1-125">-Location</span></span>
<span data-ttu-id="467a1-126">A região do Azure na qual o servidor do Analysis Services está hospedado</span><span class="sxs-lookup"><span data-stu-id="467a1-126">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="467a1-127">-Name</span></span>
<span data-ttu-id="467a1-128">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="467a1-128">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="467a1-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="467a1-130">Ler apenas a contagem de réplicas de um servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="467a1-130">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467a1-131">-ResourceGroupName</span></span>
<span data-ttu-id="467a1-132">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="467a1-132">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="467a1-133">-Sku</span></span>
<span data-ttu-id="467a1-134">O nome da SKU do servidor.</span><span class="sxs-lookup"><span data-stu-id="467a1-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="467a1-135">Os valores compatíveis são 0 ', 1 ', 2 ' são 4 ' para o nível padrão; ' B1 ', ' B2 ' para a camada básica e 1 ' para o nível de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="467a1-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="467a1-136">-Tag</span></span>
<span data-ttu-id="467a1-137">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="467a1-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467a1-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="467a1-138">-Confirm</span></span>
<span data-ttu-id="467a1-139">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="467a1-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="467a1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="467a1-140">-WhatIf</span></span>
<span data-ttu-id="467a1-141">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="467a1-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="467a1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467a1-142">CommonParameters</span></span>
<span data-ttu-id="467a1-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467a1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467a1-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467a1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467a1-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="467a1-145">INPUTS</span></span>

### <span data-ttu-id="467a1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="467a1-146">System.String</span></span>

### <span data-ttu-id="467a1-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="467a1-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="467a1-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="467a1-148">System.Int32</span></span>

### <span data-ttu-id="467a1-149">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="467a1-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="467a1-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="467a1-150">OUTPUTS</span></span>

### <span data-ttu-id="467a1-151">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="467a1-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="467a1-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="467a1-152">NOTES</span></span>
<span data-ttu-id="467a1-153">Alias: New-AzAs</span><span class="sxs-lookup"><span data-stu-id="467a1-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="467a1-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="467a1-154">RELATED LINKS</span></span>

[<span data-ttu-id="467a1-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="467a1-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="467a1-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="467a1-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
