---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: 1ba12a18c88004dcc1c6761d71fdc1983a5ba0c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431668"
---
# <span data-ttu-id="3177c-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3177c-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="3177c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3177c-102">SYNOPSIS</span></span>
<span data-ttu-id="3177c-103">Cria um segredo em um cofre de chaves a partir de um segredo em backup.</span><span class="sxs-lookup"><span data-stu-id="3177c-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3177c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3177c-104">SYNTAX</span></span>

### <span data-ttu-id="3177c-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3177c-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3177c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3177c-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3177c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3177c-107">DESCRIPTION</span></span>
<span data-ttu-id="3177c-108">O cmdlet **Restore-AzureKeyVaultSecret** cria um segredo no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="3177c-108">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="3177c-109">Esse segredo é uma réplica do segredo em backup no arquivo de entrada e tem o mesmo nome que o segredo original.</span><span class="sxs-lookup"><span data-stu-id="3177c-109">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="3177c-110">Se o cofre de chaves já tem um segredo com o mesmo nome, esse cmdlet falha em vez de substituir o segredo original.</span><span class="sxs-lookup"><span data-stu-id="3177c-110">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="3177c-111">Se o backup contiver várias versões de um segredo, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="3177c-111">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="3177c-112">O cofre de chaves no qual você restaura o segredo pode ser diferente do cofre de chaves do qual você está fazendo o backup do segredo.</span><span class="sxs-lookup"><span data-stu-id="3177c-112">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="3177c-113">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="3177c-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="3177c-114">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="3177c-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="3177c-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3177c-115">EXAMPLES</span></span>

### <span data-ttu-id="3177c-116">Exemplo 1: restaurar um segredo em backup</span><span class="sxs-lookup"><span data-stu-id="3177c-116">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="3177c-117">Esse comando restaura um segredo, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="3177c-117">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="3177c-118">OS</span><span class="sxs-lookup"><span data-stu-id="3177c-118">PARAMETERS</span></span>

### <span data-ttu-id="3177c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3177c-119">-DefaultProfile</span></span>
<span data-ttu-id="3177c-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3177c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3177c-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3177c-121">-InputFile</span></span>
<span data-ttu-id="3177c-122">Especifica o arquivo de entrada que contém o backup do segredo a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="3177c-122">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3177c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3177c-123">-InputObject</span></span>
<span data-ttu-id="3177c-124">Objeto do keyvault</span><span class="sxs-lookup"><span data-stu-id="3177c-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3177c-125">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="3177c-125">-VaultName</span></span>
<span data-ttu-id="3177c-126">Especifica o nome do cofre de chaves no qual você deseja restaurar o segredo.</span><span class="sxs-lookup"><span data-stu-id="3177c-126">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3177c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3177c-127">-Confirm</span></span>
<span data-ttu-id="3177c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3177c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3177c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3177c-129">-WhatIf</span></span>
<span data-ttu-id="3177c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3177c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3177c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3177c-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3177c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3177c-132">CommonParameters</span></span>
<span data-ttu-id="3177c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3177c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3177c-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3177c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3177c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3177c-135">INPUTS</span></span>

### <span data-ttu-id="3177c-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3177c-136">None</span></span>
<span data-ttu-id="3177c-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3177c-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3177c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3177c-138">OUTPUTS</span></span>

### <span data-ttu-id="3177c-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3177c-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="3177c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3177c-140">NOTES</span></span>

## <span data-ttu-id="3177c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3177c-141">RELATED LINKS</span></span>

[<span data-ttu-id="3177c-142">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3177c-142">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="3177c-143">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3177c-143">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="3177c-144">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3177c-144">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="3177c-145">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3177c-145">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

