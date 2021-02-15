---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: a3c3338db7fb749b3eb4d5e92c438deda0742a67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112313"
---
# <span data-ttu-id="04b1d-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="04b1d-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="04b1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="04b1d-103">Modifica uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="04b1d-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="04b1d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04b1d-104">SYNTAX</span></span>

### <span data-ttu-id="04b1d-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="04b1d-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b1d-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="04b1d-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b1d-107">DesassociateGateway</span><span class="sxs-lookup"><span data-stu-id="04b1d-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04b1d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="04b1d-108">DESCRIPTION</span></span>
<span data-ttu-id="04b1d-109">O Set-AzAnalysisServicesServer cmdlet modifica uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="04b1d-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="04b1d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="04b1d-110">EXAMPLES</span></span>

### <span data-ttu-id="04b1d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04b1d-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="04b1d-112">Modifica o servidor testserver nomeado no grupo de teste de grupo de recursos para definir as marcas como chave1:valor1 e chave2:valor2 e administrador para testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="04b1d-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="04b1d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04b1d-113">PARAMETERS</span></span>

### <span data-ttu-id="04b1d-114">-Administrador</span><span class="sxs-lookup"><span data-stu-id="04b1d-114">-Administrator</span></span>
<span data-ttu-id="04b1d-115">Uma cadeia de caracteres que representa uma lista separada por vírgulas de usuários ou grupos a serem definidos como administradores no servidor.</span><span class="sxs-lookup"><span data-stu-id="04b1d-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="04b1d-116">Os usuários ou grupos precisam ser especificados no formato UPN, por user@contoso.com exemplo, ou groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="04b1d-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="04b1d-117">-BackupBiqueContainerUri</span><span class="sxs-lookup"><span data-stu-id="04b1d-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="04b1d-118">O Uri do contêiner de blob para fazer backup do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="04b1d-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="04b1d-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="04b1d-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="04b1d-120">Modo de conexão padrão de um servidor de serviço de Análise</span><span class="sxs-lookup"><span data-stu-id="04b1d-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="04b1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b1d-121">-DefaultProfile</span></span>
<span data-ttu-id="04b1d-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="04b1d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04b1d-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="04b1d-123">-DisableBackup</span></span>
<span data-ttu-id="04b1d-124">A opção para desabilitar o contêiner de blob de backup.</span><span class="sxs-lookup"><span data-stu-id="04b1d-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="04b1d-125">Para reabilitar o contêiner de blob de backup, forneça o Uri do contêiner de blob de backup como -BackupBltContainerUri.</span><span class="sxs-lookup"><span data-stu-id="04b1d-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="04b1d-126">-DesassociateGateway</span><span class="sxs-lookup"><span data-stu-id="04b1d-126">-DisassociateGateway</span></span>
<span data-ttu-id="04b1d-127">Desassociar o recurso Gateway de um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="04b1d-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="04b1d-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="04b1d-128">-FirewallConfig</span></span>
<span data-ttu-id="04b1d-129">Configuração de firewall de um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="04b1d-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="04b1d-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="04b1d-130">-GatewayResourceId</span></span>
<span data-ttu-id="04b1d-131">ID de recurso do gateway para associar a um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="04b1d-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="04b1d-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="04b1d-132">-Name</span></span>
<span data-ttu-id="04b1d-133">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="04b1d-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="04b1d-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04b1d-134">-PassThru</span></span>
<span data-ttu-id="04b1d-135">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="04b1d-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="04b1d-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="04b1d-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="04b1d-137">Contagem de replicas somente leitura de um servidor de serviços do Analysis</span><span class="sxs-lookup"><span data-stu-id="04b1d-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="04b1d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b1d-138">-ResourceGroupName</span></span>
<span data-ttu-id="04b1d-139">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="04b1d-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="04b1d-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="04b1d-140">-Sku</span></span>
<span data-ttu-id="04b1d-141">O nome da SKU para o servidor.</span><span class="sxs-lookup"><span data-stu-id="04b1d-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="04b1d-142">Os valores com suporte são 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' para o nível Padrão; 'B1', 'B2' para o nível Básico e 'D1' para o nível Desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="04b1d-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="04b1d-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="04b1d-143">-Tag</span></span>
<span data-ttu-id="04b1d-144">Pares de valor-chave na forma de uma tabela hash definida como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="04b1d-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="04b1d-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="04b1d-145">-Confirm</span></span>
<span data-ttu-id="04b1d-146">Solicita que o usuário confirme se a operação será realizada</span><span class="sxs-lookup"><span data-stu-id="04b1d-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="04b1d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b1d-147">-WhatIf</span></span>
<span data-ttu-id="04b1d-148">Descreve as ações que a operação atual executará sem realmente executa-las</span><span class="sxs-lookup"><span data-stu-id="04b1d-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="04b1d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b1d-149">CommonParameters</span></span>
<span data-ttu-id="04b1d-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b1d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b1d-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04b1d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b1d-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="04b1d-152">INPUTS</span></span>

### <span data-ttu-id="04b1d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="04b1d-153">System.String</span></span>

### <span data-ttu-id="04b1d-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="04b1d-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="04b1d-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="04b1d-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="04b1d-156">System.Int32</span><span class="sxs-lookup"><span data-stu-id="04b1d-156">System.Int32</span></span>

### <span data-ttu-id="04b1d-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="04b1d-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="04b1d-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="04b1d-158">OUTPUTS</span></span>

### <span data-ttu-id="04b1d-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="04b1d-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="04b1d-160">Notas</span><span class="sxs-lookup"><span data-stu-id="04b1d-160">NOTES</span></span>
<span data-ttu-id="04b1d-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="04b1d-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="04b1d-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04b1d-162">RELATED LINKS</span></span>

[<span data-ttu-id="04b1d-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="04b1d-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="04b1d-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="04b1d-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
