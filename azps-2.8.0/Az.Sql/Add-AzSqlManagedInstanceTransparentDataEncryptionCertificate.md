---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: dc73939aaae76c0444307cbd1aa6bfb08711b2e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772397"
---
# <span data-ttu-id="02884-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="02884-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="02884-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02884-102">SYNOPSIS</span></span>
<span data-ttu-id="02884-103">Adiciona um certificado de criptografia de dados transparente para a instância gerenciada fornecida</span><span class="sxs-lookup"><span data-stu-id="02884-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="02884-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02884-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02884-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02884-105">DESCRIPTION</span></span>
<span data-ttu-id="02884-106">O Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adiciona um certificado de criptografia de dados transparente para a instância gerenciada fornecida</span><span class="sxs-lookup"><span data-stu-id="02884-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="02884-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02884-107">EXAMPLES</span></span>

### <span data-ttu-id="02884-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02884-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="02884-109">OS</span><span class="sxs-lookup"><span data-stu-id="02884-109">PARAMETERS</span></span>

### <span data-ttu-id="02884-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02884-110">-DefaultProfile</span></span>
<span data-ttu-id="02884-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02884-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02884-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="02884-112">-ManagedInstanceName</span></span>
<span data-ttu-id="02884-113">O nome da instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="02884-113">The managed instance name</span></span>

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

### <span data-ttu-id="02884-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02884-114">-PassThru</span></span>
<span data-ttu-id="02884-115">Na execução bem-sucedida, retorna o objeto de certificado que foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="02884-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="02884-116">-Senha</span><span class="sxs-lookup"><span data-stu-id="02884-116">-Password</span></span>
<span data-ttu-id="02884-117">A senha para certificado de criptografia de dados transparente</span><span class="sxs-lookup"><span data-stu-id="02884-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02884-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="02884-118">-PrivateBlob</span></span>
<span data-ttu-id="02884-119">O blob privado para certificado de criptografia de dados transparente</span><span class="sxs-lookup"><span data-stu-id="02884-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02884-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02884-120">-ResourceGroupName</span></span>
<span data-ttu-id="02884-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="02884-121">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02884-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02884-122">-Confirm</span></span>
<span data-ttu-id="02884-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02884-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02884-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02884-124">-WhatIf</span></span>
<span data-ttu-id="02884-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02884-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02884-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02884-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02884-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02884-127">CommonParameters</span></span>
<span data-ttu-id="02884-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02884-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02884-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02884-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02884-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02884-130">INPUTS</span></span>

### <span data-ttu-id="02884-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="02884-131">None</span></span>

## <span data-ttu-id="02884-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02884-132">OUTPUTS</span></span>

### <span data-ttu-id="02884-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02884-133">System.Boolean</span></span>

## <span data-ttu-id="02884-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02884-134">NOTES</span></span>

## <span data-ttu-id="02884-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02884-135">RELATED LINKS</span></span>