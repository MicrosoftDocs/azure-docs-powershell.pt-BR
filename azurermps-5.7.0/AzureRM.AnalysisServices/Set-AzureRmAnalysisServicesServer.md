---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 485687b0a08ca69edc77b4ee5f9510ad8a1396a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428223"
---
# <span data-ttu-id="91e49-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="91e49-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="91e49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91e49-102">SYNOPSIS</span></span>
<span data-ttu-id="91e49-103">Modifica uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91e49-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91e49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91e49-104">SYNTAX</span></span>

### <span data-ttu-id="91e49-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="91e49-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91e49-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="91e49-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91e49-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91e49-107">DESCRIPTION</span></span>
<span data-ttu-id="91e49-108">O cmdlet Set-AzureRmAnalysisServicesServer modifica uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91e49-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="91e49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91e49-109">EXAMPLES</span></span>

### <span data-ttu-id="91e49-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91e49-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="91e49-111">Modifica o servidor chamado TestServer no grupo de teste de grupo de Resource para definir as marcas como key1: valor1 e Key2: value2 e administrador para testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="91e49-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="91e49-112">OS</span><span class="sxs-lookup"><span data-stu-id="91e49-112">PARAMETERS</span></span>

### <span data-ttu-id="91e49-113">-Administrador</span><span class="sxs-lookup"><span data-stu-id="91e49-113">-Administrator</span></span>
<span data-ttu-id="91e49-114">Uma cadeia de caracteres que representa uma lista separada por vírgulas de usuários ou grupos a serem definidos como administradores no servidor.</span><span class="sxs-lookup"><span data-stu-id="91e49-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="91e49-115">Os usuários ou grupos precisam ser do formato UPN especificado, por exemplo, user@contoso.com ou groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="91e49-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="91e49-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="91e49-117">O URI do contêiner de BLOB para fazer backup do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91e49-117">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e49-118">-DefaultProfile</span></span>
<span data-ttu-id="91e49-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91e49-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-120">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="91e49-120">-DisableBackup</span></span>
<span data-ttu-id="91e49-121">A opção para desabilitar o contêiner de blob de backup.</span><span class="sxs-lookup"><span data-stu-id="91e49-121">The switch to disable backup blob container.</span></span>
<span data-ttu-id="91e49-122">Para habilitar novamente o contêiner de blob de backup, informe o URI do contêiner de blob de backup como-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="91e49-122">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBackup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="91e49-123">-Name</span></span>
<span data-ttu-id="91e49-124">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91e49-124">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91e49-125">-PassThru</span></span>
<span data-ttu-id="91e49-126">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="91e49-126">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e49-127">-ResourceGroupName</span></span>
<span data-ttu-id="91e49-128">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="91e49-128">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="91e49-129">-Sku</span></span>
<span data-ttu-id="91e49-130">O nome da SKU do servidor.</span><span class="sxs-lookup"><span data-stu-id="91e49-130">The name of the Sku for the server.</span></span>
<span data-ttu-id="91e49-131">Os valores compatíveis são 0 ', 1 ', 2 ' são 4 ' para o nível padrão; ' B1 ', ' B2 ' para a camada básica e 1 ' para o nível de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="91e49-131">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="91e49-132">-Tag</span></span>
<span data-ttu-id="91e49-133">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="91e49-133">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-134">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="91e49-134">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="91e49-135">Ler apenas a contagem de réplicas de um servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91e49-135">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-136">-Defaultconnectionmode</span><span class="sxs-lookup"><span data-stu-id="91e49-136">-DefaultConnectionMode</span></span>
<span data-ttu-id="91e49-137">Modo de conexão padrão de um servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="91e49-137">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-138">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="91e49-138">-FirewallConfig</span></span>
<span data-ttu-id="91e49-139">Configuração de firewall de um servidor de análise</span><span class="sxs-lookup"><span data-stu-id="91e49-139">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91e49-140">-Confirm</span></span>
<span data-ttu-id="91e49-141">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="91e49-141">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e49-142">-WhatIf</span></span>
<span data-ttu-id="91e49-143">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="91e49-143">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e49-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e49-144">CommonParameters</span></span>
<span data-ttu-id="91e49-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e49-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e49-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e49-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e49-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91e49-147">INPUTS</span></span>

### <span data-ttu-id="91e49-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="91e49-148">None</span></span>
<span data-ttu-id="91e49-149">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="91e49-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91e49-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91e49-150">OUTPUTS</span></span>

### <span data-ttu-id="91e49-151">Microsoft. Azure. Management. Analysis. Models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="91e49-151">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="91e49-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91e49-152">NOTES</span></span>
<span data-ttu-id="91e49-153">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="91e49-153">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="91e49-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91e49-154">RELATED LINKS</span></span>

[<span data-ttu-id="91e49-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="91e49-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="91e49-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="91e49-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
