---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: b8ce1dc13204cfeeb63f5b7eb45f57e2117da511
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785203"
---
# <span data-ttu-id="83c48-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="83c48-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="83c48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83c48-102">SYNOPSIS</span></span>
<span data-ttu-id="83c48-103">Cria um segredo em um cofre de chaves a partir de um segredo em backup.</span><span class="sxs-lookup"><span data-stu-id="83c48-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83c48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83c48-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83c48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83c48-105">DESCRIPTION</span></span>
<span data-ttu-id="83c48-106">O cmdlet **Restore-AzureKeyVaultSecret** cria um segredo no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="83c48-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="83c48-107">Esse segredo é uma réplica do segredo em backup no arquivo de entrada e tem o mesmo nome que o segredo original.</span><span class="sxs-lookup"><span data-stu-id="83c48-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="83c48-108">Se o cofre de chaves já tem um segredo com o mesmo nome, esse cmdlet falha em vez de substituir o segredo original.</span><span class="sxs-lookup"><span data-stu-id="83c48-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="83c48-109">Se o backup contiver várias versões de um segredo, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="83c48-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="83c48-110">O cofre de chaves no qual você restaura o segredo pode ser diferente do cofre de chaves do qual você está fazendo o backup do segredo.</span><span class="sxs-lookup"><span data-stu-id="83c48-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="83c48-111">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="83c48-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="83c48-112">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="83c48-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="83c48-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83c48-113">EXAMPLES</span></span>

### <span data-ttu-id="83c48-114">Exemplo 1: restaurar um segredo em backup</span><span class="sxs-lookup"><span data-stu-id="83c48-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="83c48-115">Esse comando restaura um segredo, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="83c48-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="83c48-116">OS</span><span class="sxs-lookup"><span data-stu-id="83c48-116">PARAMETERS</span></span>

### <span data-ttu-id="83c48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c48-117">-DefaultProfile</span></span>
<span data-ttu-id="83c48-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="83c48-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83c48-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="83c48-119">-InputFile</span></span>
<span data-ttu-id="83c48-120">Especifica o arquivo de entrada que contém o backup do segredo a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="83c48-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="83c48-121">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="83c48-121">-VaultName</span></span>
<span data-ttu-id="83c48-122">Especifica o nome do cofre de chaves no qual você deseja restaurar o segredo.</span><span class="sxs-lookup"><span data-stu-id="83c48-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="83c48-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="83c48-123">-Confirm</span></span>
<span data-ttu-id="83c48-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83c48-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83c48-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83c48-125">-WhatIf</span></span>
<span data-ttu-id="83c48-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="83c48-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83c48-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="83c48-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83c48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c48-128">CommonParameters</span></span>
<span data-ttu-id="83c48-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c48-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83c48-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c48-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83c48-131">INPUTS</span></span>

## <span data-ttu-id="83c48-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83c48-132">OUTPUTS</span></span>

### <span data-ttu-id="83c48-133">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="83c48-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="83c48-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83c48-134">NOTES</span></span>

## <span data-ttu-id="83c48-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83c48-135">RELATED LINKS</span></span>

[<span data-ttu-id="83c48-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="83c48-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="83c48-137">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="83c48-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="83c48-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="83c48-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="83c48-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="83c48-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

