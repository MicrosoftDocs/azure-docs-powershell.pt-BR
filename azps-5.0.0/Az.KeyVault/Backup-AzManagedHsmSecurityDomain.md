---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: 10a54afa8a6ef2e37beebd9d6cdcd304b2d13979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280505"
---
# <span data-ttu-id="13c7e-101">Backup-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="13c7e-101">Backup-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="13c7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="13c7e-103">Faz backup dos dados do domínio de segurança de um HSM gerenciado para restauração.</span><span class="sxs-lookup"><span data-stu-id="13c7e-103">Backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="13c7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13c7e-104">SYNTAX</span></span>

### <span data-ttu-id="13c7e-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="13c7e-105">ByName (Default)</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13c7e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="13c7e-106">ByInputObject</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13c7e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13c7e-107">DESCRIPTION</span></span>
<span data-ttu-id="13c7e-108">Esse cmdlet faz backup dos dados do domínio de segurança de um HSM gerenciado para restauração.</span><span class="sxs-lookup"><span data-stu-id="13c7e-108">This cmdlet backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="13c7e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13c7e-109">EXAMPLES</span></span>

### <span data-ttu-id="13c7e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13c7e-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="13c7e-111">Esse comando recupera o HSM gerenciado chamado testmhsm e salva um backup desse domínio de segurança do HSM gerenciado para o arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="13c7e-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="13c7e-112">OS</span><span class="sxs-lookup"><span data-stu-id="13c7e-112">PARAMETERS</span></span>

### <span data-ttu-id="13c7e-113">-Certificados</span><span class="sxs-lookup"><span data-stu-id="13c7e-113">-Certificates</span></span>
<span data-ttu-id="13c7e-114">Caminhos para os certificados que são usados para criptografar os dados do domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="13c7e-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c7e-115">-DefaultProfile</span></span>
<span data-ttu-id="13c7e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13c7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c7e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="13c7e-117">-Force</span></span>
<span data-ttu-id="13c7e-118">Especifique se deseja substituir o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="13c7e-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="13c7e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13c7e-119">-InputObject</span></span>
<span data-ttu-id="13c7e-120">Objeto que representa um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="13c7e-120">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13c7e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="13c7e-121">-Name</span></span>
<span data-ttu-id="13c7e-122">Nome do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="13c7e-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c7e-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="13c7e-123">-OutputPath</span></span>
<span data-ttu-id="13c7e-124">Especifique o caminho onde os dados do domínio de segurança serão baixados.</span><span class="sxs-lookup"><span data-stu-id="13c7e-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c7e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13c7e-125">-PassThru</span></span>
<span data-ttu-id="13c7e-126">Quando especificado, um booliano será retornado quando o cmdlet for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="13c7e-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="13c7e-127">-Quorum</span><span class="sxs-lookup"><span data-stu-id="13c7e-127">-Quorum</span></span>
<span data-ttu-id="13c7e-128">O número mínimo de partilhas necessários para descriptografar o domínio de segurança para recuperação.</span><span class="sxs-lookup"><span data-stu-id="13c7e-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c7e-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="13c7e-129">-Confirm</span></span>
<span data-ttu-id="13c7e-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13c7e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13c7e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13c7e-131">-WhatIf</span></span>
<span data-ttu-id="13c7e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="13c7e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13c7e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13c7e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13c7e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c7e-134">CommonParameters</span></span>
<span data-ttu-id="13c7e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c7e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c7e-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13c7e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c7e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13c7e-137">INPUTS</span></span>

### <span data-ttu-id="13c7e-138">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="13c7e-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="13c7e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13c7e-139">OUTPUTS</span></span>

### <span data-ttu-id="13c7e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13c7e-140">System.Boolean</span></span>

## <span data-ttu-id="13c7e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13c7e-141">NOTES</span></span>

## <span data-ttu-id="13c7e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13c7e-142">RELATED LINKS</span></span>
