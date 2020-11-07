---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: d13ffe73ada97ba68825beeb1769572767b3561a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941965"
---
# <span data-ttu-id="91f2b-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="91f2b-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="91f2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="91f2b-103">Modifica uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91f2b-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="91f2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91f2b-104">SYNTAX</span></span>

### <span data-ttu-id="91f2b-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="91f2b-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91f2b-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="91f2b-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91f2b-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="91f2b-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91f2b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91f2b-108">DESCRIPTION</span></span>
<span data-ttu-id="91f2b-109">O cmdlet Set-AzAnalysisServicesServer modifica uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91f2b-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="91f2b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91f2b-110">EXAMPLES</span></span>

### <span data-ttu-id="91f2b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91f2b-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="91f2b-112">Modifica o servidor chamado TestServer no grupo de teste de grupo de Resource para definir as marcas como key1: valor1 e Key2: value2 e administrador para testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="91f2b-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="91f2b-113">OS</span><span class="sxs-lookup"><span data-stu-id="91f2b-113">PARAMETERS</span></span>

### <span data-ttu-id="91f2b-114">-Administrador</span><span class="sxs-lookup"><span data-stu-id="91f2b-114">-Administrator</span></span>
<span data-ttu-id="91f2b-115">Uma cadeia de caracteres que representa uma lista separada por vírgulas de usuários ou grupos a serem definidos como administradores no servidor.</span><span class="sxs-lookup"><span data-stu-id="91f2b-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="91f2b-116">Os usuários ou grupos precisam ser do formato UPN especificado, por exemplo, user@contoso.com ou groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="91f2b-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f2b-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="91f2b-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="91f2b-118">O URI do contêiner de BLOB para fazer backup do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91f2b-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f2b-119">-Defaultconnectionmode</span><span class="sxs-lookup"><span data-stu-id="91f2b-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="91f2b-120">Modo de conexão padrão de um servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91f2b-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="91f2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f2b-121">-DefaultProfile</span></span>
<span data-ttu-id="91f2b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91f2b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91f2b-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="91f2b-123">-DisableBackup</span></span>
<span data-ttu-id="91f2b-124">A opção para desabilitar o contêiner de blob de backup.</span><span class="sxs-lookup"><span data-stu-id="91f2b-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="91f2b-125">Para habilitar novamente o contêiner de blob de backup, informe o URI do contêiner de blob de backup como-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="91f2b-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f2b-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="91f2b-126">-DisassociateGateway</span></span>
<span data-ttu-id="91f2b-127">Desassociar o recurso de gateway de um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="91f2b-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f2b-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="91f2b-128">-FirewallConfig</span></span>
<span data-ttu-id="91f2b-129">Configuração de firewall de um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="91f2b-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="91f2b-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="91f2b-130">-GatewayResourceId</span></span>
<span data-ttu-id="91f2b-131">ID do recurso do gateway para associar a um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="91f2b-131">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f2b-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="91f2b-132">-Name</span></span>
<span data-ttu-id="91f2b-133">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91f2b-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="91f2b-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91f2b-134">-PassThru</span></span>
<span data-ttu-id="91f2b-135">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="91f2b-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="91f2b-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="91f2b-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="91f2b-137">Ler apenas a contagem de réplicas de um servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91f2b-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="91f2b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f2b-138">-ResourceGroupName</span></span>
<span data-ttu-id="91f2b-139">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="91f2b-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f2b-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="91f2b-140">-Sku</span></span>
<span data-ttu-id="91f2b-141">O nome da SKU do servidor.</span><span class="sxs-lookup"><span data-stu-id="91f2b-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="91f2b-142">Os valores compatíveis são 0 ', 1 ', 2 ' são 4 ' para o nível padrão; ' B1 ', ' B2 ' para a camada básica e 1 ' para o nível de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="91f2b-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f2b-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="91f2b-143">-Tag</span></span>
<span data-ttu-id="91f2b-144">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="91f2b-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f2b-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91f2b-145">-Confirm</span></span>
<span data-ttu-id="91f2b-146">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="91f2b-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="91f2b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f2b-147">-WhatIf</span></span>
<span data-ttu-id="91f2b-148">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="91f2b-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="91f2b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f2b-149">CommonParameters</span></span>
<span data-ttu-id="91f2b-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f2b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f2b-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f2b-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f2b-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91f2b-152">INPUTS</span></span>

### <span data-ttu-id="91f2b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="91f2b-153">System.String</span></span>

### <span data-ttu-id="91f2b-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="91f2b-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="91f2b-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="91f2b-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="91f2b-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="91f2b-156">System.Int32</span></span>

### <span data-ttu-id="91f2b-157">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="91f2b-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="91f2b-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91f2b-158">OUTPUTS</span></span>

### <span data-ttu-id="91f2b-159">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="91f2b-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="91f2b-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91f2b-160">NOTES</span></span>
<span data-ttu-id="91f2b-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="91f2b-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="91f2b-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91f2b-162">RELATED LINKS</span></span>

[<span data-ttu-id="91f2b-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="91f2b-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="91f2b-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="91f2b-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
