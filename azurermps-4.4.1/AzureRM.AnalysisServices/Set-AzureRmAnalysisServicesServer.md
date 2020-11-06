---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427056"
---
# <span data-ttu-id="9dd5a-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9dd5a-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="9dd5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9dd5a-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd5a-103">Modifica uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9dd5a-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dd5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dd5a-104">SYNTAX</span></span>

### <span data-ttu-id="9dd5a-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="9dd5a-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dd5a-106">Desabilitar backup</span><span class="sxs-lookup"><span data-stu-id="9dd5a-106">Disable Backup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dd5a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9dd5a-107">DESCRIPTION</span></span>
<span data-ttu-id="9dd5a-108">O cmdlet Set-AzureRmAnalysisServicesServer modifica uma instância do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9dd5a-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="9dd5a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9dd5a-109">EXAMPLES</span></span>

### <span data-ttu-id="9dd5a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9dd5a-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="9dd5a-111">Modifica o servidor chamado TestServer no grupo de teste de grupo de Resource para definir as marcas como key1: valor1 e Key2: value2 e administrador para testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9dd5a-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="9dd5a-112">OS</span><span class="sxs-lookup"><span data-stu-id="9dd5a-112">PARAMETERS</span></span>

### <span data-ttu-id="9dd5a-113">-Administrador</span><span class="sxs-lookup"><span data-stu-id="9dd5a-113">-Administrator</span></span>
<span data-ttu-id="9dd5a-114">Uma cadeia de caracteres que representa uma lista separada por vírgulas de usuários ou grupos a serem definidos como administradores no servidor.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="9dd5a-115">Os usuários ou grupos precisam ser do formato UPN especificado, por exemplo, user@contoso.com ou groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9dd5a-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="9dd5a-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="9dd5a-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="9dd5a-117">O URI do contêiner de BLOB para fazer backup do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9dd5a-117">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="9dd5a-118">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="9dd5a-118">-DisableBackup</span></span>
<span data-ttu-id="9dd5a-119">A opção para desabilitar o contêiner de blob de backup.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-119">The switch to disable backup blob container.</span></span>
<span data-ttu-id="9dd5a-120">Para habilitar novamente o contêiner de blob de backup, informe o URI do contêiner de blob de backup como-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-120">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd5a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9dd5a-121">-Name</span></span>
<span data-ttu-id="9dd5a-122">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9dd5a-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="9dd5a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dd5a-123">-PassThru</span></span>
<span data-ttu-id="9dd5a-124">Retornará os detalhes do servidor excluído se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="9dd5a-124">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="9dd5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="9dd5a-126">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="9dd5a-126">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="9dd5a-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="9dd5a-127">-Sku</span></span>
<span data-ttu-id="9dd5a-128">O nome da SKU do servidor.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-128">The name of the Sku for the server.</span></span>
<span data-ttu-id="9dd5a-129">Os valores compatíveis são 0 ', 1 ', 2 ' são 4 ' para o nível padrão; ' B1 ', ' B2 ' para a camada básica e 1 ' para o nível de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-129">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="9dd5a-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="9dd5a-130">-Tag</span></span>
<span data-ttu-id="9dd5a-131">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-131">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="9dd5a-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9dd5a-132">-Confirm</span></span>
<span data-ttu-id="9dd5a-133">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="9dd5a-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="9dd5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd5a-134">-WhatIf</span></span>
<span data-ttu-id="9dd5a-135">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="9dd5a-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="9dd5a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd5a-136">-DefaultProfile</span></span>
<span data-ttu-id="9dd5a-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd5a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd5a-138">CommonParameters</span></span>
<span data-ttu-id="9dd5a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd5a-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd5a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd5a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9dd5a-141">INPUTS</span></span>

## <span data-ttu-id="9dd5a-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9dd5a-142">OUTPUTS</span></span>

### <span data-ttu-id="9dd5a-143">Microsoft. Azure. Management. Analysis. Models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9dd5a-143">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="9dd5a-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9dd5a-144">NOTES</span></span>
<span data-ttu-id="9dd5a-145">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="9dd5a-145">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="9dd5a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dd5a-146">RELATED LINKS</span></span>

[<span data-ttu-id="9dd5a-147">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9dd5a-147">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="9dd5a-148">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9dd5a-148">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
