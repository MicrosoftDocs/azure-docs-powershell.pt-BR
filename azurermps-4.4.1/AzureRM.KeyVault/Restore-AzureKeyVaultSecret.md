---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: bd619f6c4ec9891972d23738c1f2510cba0e2272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603113"
---
# <span data-ttu-id="94819-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94819-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="94819-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94819-102">SYNOPSIS</span></span>
<span data-ttu-id="94819-103">Cria um segredo em um cofre de chaves a partir de um segredo em backup.</span><span class="sxs-lookup"><span data-stu-id="94819-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94819-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94819-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94819-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94819-105">DESCRIPTION</span></span>
<span data-ttu-id="94819-106">O cmdlet **Restore-AzureKeyVaultSecret** cria um segredo no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="94819-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="94819-107">Esse segredo é uma réplica do segredo em backup no arquivo de entrada e tem o mesmo nome que o segredo original.</span><span class="sxs-lookup"><span data-stu-id="94819-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="94819-108">Se o cofre de chaves já tem um segredo com o mesmo nome, esse cmdlet falha em vez de substituir o segredo original.</span><span class="sxs-lookup"><span data-stu-id="94819-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="94819-109">Se o backup contiver várias versões de um segredo, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="94819-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="94819-110">O cofre de chaves no qual você restaura o segredo pode ser diferente do cofre de chaves do qual você está fazendo o backup do segredo.</span><span class="sxs-lookup"><span data-stu-id="94819-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="94819-111">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="94819-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="94819-112">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="94819-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="94819-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94819-113">EXAMPLES</span></span>

### <span data-ttu-id="94819-114">Exemplo 1: restaurar um segredo em backup</span><span class="sxs-lookup"><span data-stu-id="94819-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="94819-115">Esse comando restaura um segredo, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="94819-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="94819-116">OS</span><span class="sxs-lookup"><span data-stu-id="94819-116">PARAMETERS</span></span>

### <span data-ttu-id="94819-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="94819-117">-InputFile</span></span>
<span data-ttu-id="94819-118">Especifica o arquivo de entrada que contém o backup do segredo a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="94819-118">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94819-119">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="94819-119">-VaultName</span></span>
<span data-ttu-id="94819-120">Especifica o nome do cofre de chaves no qual você deseja restaurar o segredo.</span><span class="sxs-lookup"><span data-stu-id="94819-120">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="94819-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94819-121">-Confirm</span></span>
<span data-ttu-id="94819-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94819-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94819-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94819-123">-WhatIf</span></span>
<span data-ttu-id="94819-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94819-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94819-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94819-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94819-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94819-126">-DefaultProfile</span></span>
<span data-ttu-id="94819-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94819-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94819-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94819-128">CommonParameters</span></span>
<span data-ttu-id="94819-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94819-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94819-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94819-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94819-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94819-131">INPUTS</span></span>

## <span data-ttu-id="94819-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94819-132">OUTPUTS</span></span>

### <span data-ttu-id="94819-133">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="94819-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="94819-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94819-134">NOTES</span></span>

## <span data-ttu-id="94819-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94819-135">RELATED LINKS</span></span>

[<span data-ttu-id="94819-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94819-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="94819-137">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94819-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="94819-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94819-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="94819-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94819-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

