---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 4af261f10a4d5f3d7228f31b511a092600cb93bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885446"
---
# <span data-ttu-id="ad08f-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ad08f-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="ad08f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad08f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad08f-103">Restaura um certificado em um cofre de chaves de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="ad08f-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="ad08f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ad08f-104">SYNTAX</span></span>

### <span data-ttu-id="ad08f-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ad08f-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad08f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad08f-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad08f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad08f-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad08f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ad08f-108">DESCRIPTION</span></span>
<span data-ttu-id="ad08f-109">O cmdlet **Restore-AzKeyVaultCertificate** cria um certificado no cofre de chaves especificado de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="ad08f-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="ad08f-110">Esse certificado é uma réplica do certificado de backup no arquivo de entrada e tem o mesmo nome do certificado original.</span><span class="sxs-lookup"><span data-stu-id="ad08f-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="ad08f-111">Se o cofre de chaves já contiver um certificado com o mesmo nome, esse cmdlet falhará em vez de sobrescrever o certificado original.</span><span class="sxs-lookup"><span data-stu-id="ad08f-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="ad08f-112">Se o backup contiver várias versões de um certificado, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="ad08f-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="ad08f-113">O cofre de chaves em que você restaura o certificado pode ser diferente do cofre de chaves de onde você fez o backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="ad08f-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="ad08f-114">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="ad08f-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ad08f-115">Consulte o Centro de Confiança do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para geografias.</span><span class="sxs-lookup"><span data-stu-id="ad08f-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ad08f-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad08f-116">EXAMPLES</span></span>

### <span data-ttu-id="ad08f-117">Exemplo 1: Restaurar um certificado com backup</span><span class="sxs-lookup"><span data-stu-id="ad08f-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="ad08f-118">Este comando restaura um certificado, incluindo todas as suas versões, do arquivo de backup chamado Backup.blob para o cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ad08f-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="ad08f-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ad08f-119">PARAMETERS</span></span>

### <span data-ttu-id="ad08f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad08f-120">-DefaultProfile</span></span>
<span data-ttu-id="ad08f-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad08f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad08f-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ad08f-122">-InputFile</span></span>
<span data-ttu-id="ad08f-123">Arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ad08f-123">Input file.</span></span>
<span data-ttu-id="ad08f-124">O arquivo de entrada que contém o blob de backup</span><span class="sxs-lookup"><span data-stu-id="ad08f-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="ad08f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad08f-125">-InputObject</span></span>
<span data-ttu-id="ad08f-126">Objeto KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad08f-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad08f-127">-ResourceId</span></span>
<span data-ttu-id="ad08f-128">ID do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad08f-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ad08f-129">-VaultName</span></span>
<span data-ttu-id="ad08f-130">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="ad08f-130">Vault name.</span></span>
<span data-ttu-id="ad08f-131">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ad08f-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad08f-132">-Confirm</span></span>
<span data-ttu-id="ad08f-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad08f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad08f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad08f-134">-WhatIf</span></span>
<span data-ttu-id="ad08f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad08f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad08f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad08f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad08f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad08f-137">CommonParameters</span></span>
<span data-ttu-id="ad08f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad08f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad08f-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad08f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad08f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad08f-140">INPUTS</span></span>

### <span data-ttu-id="ad08f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ad08f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ad08f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ad08f-142">System.String</span></span>

## <span data-ttu-id="ad08f-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ad08f-143">OUTPUTS</span></span>

### <span data-ttu-id="ad08f-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ad08f-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="ad08f-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="ad08f-145">NOTES</span></span>

## <span data-ttu-id="ad08f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad08f-146">RELATED LINKS</span></span>
