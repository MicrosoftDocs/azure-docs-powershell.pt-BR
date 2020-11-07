---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 8df9d0b5149ef3b22477be1f2316bf499a3b1c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772664"
---
# <span data-ttu-id="f2cdc-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="f2cdc-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="f2cdc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cdc-103">Use somente para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-103">Use for troubleshooting only.</span></span> <span data-ttu-id="f2cdc-104">Esse comando irá reverter o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="f2cdc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2cdc-105">SYNTAX</span></span>

### <span data-ttu-id="f2cdc-106">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2cdc-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2cdc-107">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="f2cdc-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2cdc-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2cdc-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2cdc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2cdc-109">DESCRIPTION</span></span>
<span data-ttu-id="f2cdc-110">Esse comando irá rolar o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="f2cdc-111">Isso deve ser usado em cenários de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="f2cdc-112">Ao chamar esse comando, o certificado do servidor é substituído, atualizando o serviço de sincronização de armazenamento com o qual esse servidor está registrado também, enviando a parte pública da chave.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="f2cdc-113">Como um novo certificado é gerado, o tempo de expiração dessa CERT também é atualizado.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="f2cdc-114">Esse comando também pode ser usado para atualizar um certificado expirado.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="f2cdc-115">Isso pode acontecer se um servidor estiver offline por um período de tempo prolongado.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="f2cdc-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2cdc-116">EXAMPLES</span></span>

### <span data-ttu-id="f2cdc-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2cdc-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="f2cdc-118">Esse comando irá reverter o certificado do servidor local e informar o serviço de sincronização de armazenamento correspondente da nova identidade do servidor, de maneira segura.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="f2cdc-119">OS</span><span class="sxs-lookup"><span data-stu-id="f2cdc-119">PARAMETERS</span></span>

### <span data-ttu-id="f2cdc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2cdc-120">-DefaultProfile</span></span>
<span data-ttu-id="f2cdc-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2cdc-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f2cdc-122">-ParentObject</span></span>
<span data-ttu-id="f2cdc-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2cdc-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f2cdc-124">-ParentResourceId</span></span>
<span data-ttu-id="f2cdc-125">ID do recurso pai StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f2cdc-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2cdc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2cdc-126">-PassThru</span></span>
<span data-ttu-id="f2cdc-127">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f2cdc-128">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f2cdc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2cdc-129">-ResourceGroupName</span></span>
<span data-ttu-id="f2cdc-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2cdc-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f2cdc-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="f2cdc-132">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-132">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2cdc-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2cdc-133">-Confirm</span></span>
<span data-ttu-id="f2cdc-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2cdc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2cdc-135">-WhatIf</span></span>
<span data-ttu-id="f2cdc-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2cdc-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2cdc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cdc-138">CommonParameters</span></span>
<span data-ttu-id="f2cdc-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cdc-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2cdc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cdc-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2cdc-141">INPUTS</span></span>

### <span data-ttu-id="f2cdc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f2cdc-142">System.String</span></span>

### <span data-ttu-id="f2cdc-143">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f2cdc-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f2cdc-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2cdc-144">OUTPUTS</span></span>

### <span data-ttu-id="f2cdc-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="f2cdc-145">System.Object</span></span>
## <span data-ttu-id="f2cdc-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2cdc-146">NOTES</span></span>

## <span data-ttu-id="f2cdc-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2cdc-147">RELATED LINKS</span></span>