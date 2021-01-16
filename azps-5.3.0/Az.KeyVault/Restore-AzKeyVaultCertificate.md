---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428302"
---
# <span data-ttu-id="cb76f-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cb76f-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="cb76f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb76f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb76f-103">Restaura um certificado em um cofre de chaves de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="cb76f-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="cb76f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb76f-104">SYNTAX</span></span>

### <span data-ttu-id="cb76f-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb76f-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb76f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb76f-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb76f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb76f-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb76f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb76f-108">DESCRIPTION</span></span>
<span data-ttu-id="cb76f-109">O cmdlet **Restore-AzKeyVaultCertificate** cria um certificado no cofre de chaves especificado a partir de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="cb76f-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="cb76f-110">Esse certificado é uma réplica do certificado de backup no arquivo de entrada e tem o mesmo nome que o certificado original.</span><span class="sxs-lookup"><span data-stu-id="cb76f-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="cb76f-111">Se o cofre de chaves já contiver um certificado com o mesmo nome, esse cmdlet falha em vez de substituir o certificado original.</span><span class="sxs-lookup"><span data-stu-id="cb76f-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="cb76f-112">Se o backup contiver várias versões de um certificado, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="cb76f-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="cb76f-113">O cofre de chaves no qual você restaura o certificado pode ser diferente do cofre de chaves do qual você tem o backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="cb76f-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="cb76f-114">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="cb76f-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="cb76f-115">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="cb76f-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="cb76f-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb76f-116">EXAMPLES</span></span>

### <span data-ttu-id="cb76f-117">Exemplo 1: restaurar um certificado de backup</span><span class="sxs-lookup"><span data-stu-id="cb76f-117">Example 1: Restore a backed-up certificate</span></span>
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

<span data-ttu-id="cb76f-118">Esse comando restaura um certificado, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb76f-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="cb76f-119">OS</span><span class="sxs-lookup"><span data-stu-id="cb76f-119">PARAMETERS</span></span>

### <span data-ttu-id="cb76f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb76f-120">-DefaultProfile</span></span>
<span data-ttu-id="cb76f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb76f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb76f-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="cb76f-122">-InputFile</span></span>
<span data-ttu-id="cb76f-123">Arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="cb76f-123">Input file.</span></span>
<span data-ttu-id="cb76f-124">O arquivo de entrada que contém o blob com backup</span><span class="sxs-lookup"><span data-stu-id="cb76f-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="cb76f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb76f-125">-InputObject</span></span>
<span data-ttu-id="cb76f-126">Objeto do keyvault</span><span class="sxs-lookup"><span data-stu-id="cb76f-126">KeyVault object</span></span>

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

### <span data-ttu-id="cb76f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb76f-127">-ResourceId</span></span>
<span data-ttu-id="cb76f-128">ID do recurso do keyvault</span><span class="sxs-lookup"><span data-stu-id="cb76f-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="cb76f-129">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="cb76f-129">-VaultName</span></span>
<span data-ttu-id="cb76f-130">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="cb76f-130">Vault name.</span></span>
<span data-ttu-id="cb76f-131">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="cb76f-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="cb76f-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb76f-132">-Confirm</span></span>
<span data-ttu-id="cb76f-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb76f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb76f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb76f-134">-WhatIf</span></span>
<span data-ttu-id="cb76f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb76f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb76f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb76f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb76f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb76f-137">CommonParameters</span></span>
<span data-ttu-id="cb76f-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb76f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb76f-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb76f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb76f-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb76f-140">INPUTS</span></span>

### <span data-ttu-id="cb76f-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cb76f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="cb76f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cb76f-142">System.String</span></span>

## <span data-ttu-id="cb76f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb76f-143">OUTPUTS</span></span>

### <span data-ttu-id="cb76f-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cb76f-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="cb76f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb76f-145">NOTES</span></span>

## <span data-ttu-id="cb76f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb76f-146">RELATED LINKS</span></span>
