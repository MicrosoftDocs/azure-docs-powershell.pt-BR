---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 1fb58d348af5f507e1bd3c8451f12918c69b309b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441038"
---
# <span data-ttu-id="9eb6a-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9eb6a-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="9eb6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9eb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb6a-103">Cria uma chave em um cofre de chaves de uma chave com backup.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eb6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9eb6a-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eb6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9eb6a-105">DESCRIPTION</span></span>
<span data-ttu-id="9eb6a-106">O cmdlet **Restore-AzureKeyVaultKey** cria uma chave no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="9eb6a-107">Essa chave é uma réplica da chave com backup no arquivo de entrada e tem o mesmo nome da chave original.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="9eb6a-108">Se o cofre de chaves já tiver uma chave com o mesmo nome, esse cmdlet falha em vez de substituir a chave original.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="9eb6a-109">Se o backup contiver várias versões de uma chave, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="9eb6a-110">O cofre de chaves no qual você restaura a chave pode ser diferente do cofre de chaves do qual você tem o backup da chave.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="9eb6a-111">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="9eb6a-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="9eb6a-112">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="9eb6a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9eb6a-113">EXAMPLES</span></span>

### <span data-ttu-id="9eb6a-114">Exemplo 1: restaurar uma chave de backup</span><span class="sxs-lookup"><span data-stu-id="9eb6a-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="9eb6a-115">Esse comando restaura uma chave, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="9eb6a-116">OS</span><span class="sxs-lookup"><span data-stu-id="9eb6a-116">PARAMETERS</span></span>

### <span data-ttu-id="9eb6a-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="9eb6a-117">-InputFile</span></span>
<span data-ttu-id="9eb6a-118">Especifica o arquivo de entrada que contém o backup da chave a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-118">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb6a-119">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="9eb6a-119">-VaultName</span></span>
<span data-ttu-id="9eb6a-120">Especifica o nome do cofre de chaves no qual a chave será restaurada.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-120">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="9eb6a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9eb6a-121">-Confirm</span></span>
<span data-ttu-id="9eb6a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eb6a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb6a-123">-WhatIf</span></span>
<span data-ttu-id="9eb6a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eb6a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eb6a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb6a-126">-DefaultProfile</span></span>
<span data-ttu-id="9eb6a-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eb6a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb6a-128">CommonParameters</span></span>
<span data-ttu-id="9eb6a-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb6a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb6a-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eb6a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb6a-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9eb6a-131">INPUTS</span></span>

## <span data-ttu-id="9eb6a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9eb6a-132">OUTPUTS</span></span>

### <span data-ttu-id="9eb6a-133">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="9eb6a-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="9eb6a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9eb6a-134">NOTES</span></span>

## <span data-ttu-id="9eb6a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9eb6a-135">RELATED LINKS</span></span>

[<span data-ttu-id="9eb6a-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9eb6a-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="9eb6a-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9eb6a-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="9eb6a-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9eb6a-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="9eb6a-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9eb6a-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

